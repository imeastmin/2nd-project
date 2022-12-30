# 2차 프로젝트 노르딕워킹
* 기간: 2022. 11. 28 ~ 2022. 12. 16<br>
* 아키텍쳐: 클라이언트 서버 간 API 통신 방식<br>
* Swagger: http://localhost/swagger-ui/index.html
> <img width="1312" alt="image" src="https://user-images.githubusercontent.com/51441191/210045224-076d2faf-cdd2-415e-8075-6cdc1628cc0f.png">

<br><br>

- ## ISSUE
1. JACKSON NAME RULE에 따른 Property 이름 변경
2. 클라이언트 전송 데이터를 받아오는 애노테이션의 차이점(@RequestParam, @PathVariable ...)
3. HTTP 프로토콜 보안 CORS 대처
4. REST API 방식에서의 파일 업로드 처리
> _자세한 트러블슈팅_<br>
> https://eastmin.notion.site/3-Record-8da9e60b938143d2a666dcd4b23ae78c

- ## 구현
1. HTTP 프로토콜 4가지 Method로 클라이언트와 서버 간의 통신
> <img width="549" alt="image" src="https://user-images.githubusercontent.com/51441191/210046490-88b9171a-cad2-41ba-ab87-2939028ed725.png">
> <img width="549" alt="image" src="https://user-images.githubusercontent.com/51441191/210046586-a249bb86-8ddd-4e7a-a243-a4a17adf477a.png">

2. Front-End 프로젝트에서는 Ajax로 서버와 통신
> <img width="549" alt="image" src="https://user-images.githubusercontent.com/51441191/210046669-eb7087b7-35c5-4bd6-9c91-4f7be0a67364.png">

3. 원하는 데이터 출력을 위해 Join을 활용
> <img width="549" alt="image" src="https://user-images.githubusercontent.com/51441191/210046744-6fccd452-453a-47b3-b90f-0093366539e3.png">

4. DataBase Index를 활용<br><br>
5. 동아리 소개 및 기원 페이지 CRUD
> <img width="879" alt="image" src="https://user-images.githubusercontent.com/51441191/210046857-f2a7bdff-a3de-44bc-971f-c8109b7ea79f.png">
> <img width="879" alt="image" src="https://user-images.githubusercontent.com/51441191/210046910-04d7ae61-88b3-4818-a0c4-fec0831e6fed.png"><br>
> * 수정 시 이미 업로드 되어 있는 사진을 1개씩 삭제 처리할 수 있음.<br>

6. 게시판 기능 + 다중 파일 업로드 처리
> <img width="1413" alt="image" src="https://user-images.githubusercontent.com/51441191/210047159-e01bb66b-2744-4c97-be88-e5a24ee5bd9e.png"><br>
> * 클라이언트가 업로드 한 사진으로 썸네일 설정<br><br>
> <img width="1092" alt="image" src="https://user-images.githubusercontent.com/51441191/210047357-3317df9a-cef4-4a3f-bff2-0508b7cd83c4.png"><br>
> * 작성 기능 - 댓글허용 여부에 따라 댓글 사용 여부를 설정할 수 있음.<br><br>
> <img width="1174" alt="image" src="https://user-images.githubusercontent.com/51441191/210047577-0e9078be-8f9a-4186-bcfc-d82db354d9d0.png"><br>
> * 본인이 작성한 글만 수정 및 삭제 버튼이 활성화 됨.<br>
> * 댓글 설정을 하지 않으면 사진과 같은 메시지 출력.<br><br>
> <img width="724" alt="image" src="https://user-images.githubusercontent.com/51441191/210047757-6da7d6d3-d642-4e8d-aa77-a6f4d770a797.png"><br>
> * 수정 기능<br><br>
> <img width="1120" alt="image" src="https://user-images.githubusercontent.com/51441191/210047828-5c82fdb1-f2f6-4f50-8518-069c0ce71c71.png"><br>
> * 댓글 허용을 하게 되면 사진과 같은 댓글 작성 창이 출력됨.<br><br>
> <img width="857" alt="image" src="https://user-images.githubusercontent.com/51441191/210047890-c17ad2ae-b045-477c-a314-fa75523bd375.png"><br>
> * 댓글을 작성한 본인에게만 수정 삭제 버튼이 활성화 됨.<br><br>
> <img width="857" alt="image" src="https://user-images.githubusercontent.com/51441191/210047976-73cbda8d-7a69-44bf-a606-8a357761a754.png"><br>
> * 수정 버튼을 누르게 되면 수정 텍스트 창이 출력 됨.<br><br>
> <img width="857" alt="image" src="https://user-images.githubusercontent.com/51441191/210048026-26c5dfeb-4e0e-45f5-91a7-eb60039eaf5c.png"><br>
> * 수정한 결과<br><br>
> <img width="857" alt="image" src="https://user-images.githubusercontent.com/51441191/210048050-a71c6b14-3dba-4eea-9a1e-d66b73dbd97d.png"><br>
> * 삭제 확인 Confirm에서 확인을 누르게 되면 정상적으로 삭제<br>
> * 삭제한 결과<br><br>

7. 검색기능 - SORT 정렬
> <img width="857" alt="image" src="https://user-images.githubusercontent.com/51441191/210048412-c350338d-8983-4a47-b8e7-97bdc4cdfa53.png"><br>
> * 4개의 검색 타입<br><br>
> <img width="1141" alt="image" src="https://user-images.githubusercontent.com/51441191/210048512-6202de31-e437-40f4-8355-6d7c895d9498.png"><br>
> * 검색결과<br><br>
> <img width="996" alt="image" src="https://user-images.githubusercontent.com/51441191/210048570-a2e0850e-04d9-47c2-8b31-7f7ca1495b47.png"><br>
> * 검색 결과에서 페이지 이동<br><br>

- ## 개선해야 할 사항
  - Hateoas 적용하여 RESTful하게 개선
  - Exception Handling
  - Security 적용
  - FTP 서버 구축 
