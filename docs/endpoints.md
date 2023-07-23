# Endpoints for the Compax App
**********************************************************************************

- default

    - `GET / Root`
    - `GET /search/classrooms`: Query Classrooms By Parameters
    - `GET /search/buildings`: Query Buildings By Parameters
    - `GET /search/labs`: Query Labs By Parameters
    - `GET /search/offices`: Query Offices By Parameters

- users

    - `GET /i/{reference}` Get User By Reference
GET /i/{uuid} Get User By Uuid
GET /i/{username} Get User By Username
POST /i/new Create User
POST /i/admin/new Create Admin
POST /i/officer/new Create Officer

- auth
0.1.0 OAS 3.1
GET /auth/signin Sign In
POST /auth/signout Sign Out
POST /auth/signup Sign Up
POST /auth/admin/signup Sign Up Admin
POST /auth/officer/signup Sign Up Examofficer

- classrooms
GET /classrooms/ Get All Classrooms
GET /classroom/{classroom_id} Get Classroom
PUT /classrooms/{classroom_id} Update Classroom
DELETE /classrooms/{classroom_id} Delete Classroom
POST /classrooms/new Create Classroom

- buildings
GET /buildings/ Get All Buildings
GET /buildings/{building_id} Get Building
PUT /buildings/{building_id} Update Building
DELETE /buildings/{building_id} Delete Building
POST /buildings/new Create Building

- labs
GET /labs/ Get All Labs
GET /labs/{lab_id} Get Lab
PUT /labs/{lab_id} Update Lab
DELETE /labs/{lab_id} Delete Lab
POST /labs/new Create Lab

- offices
GET /offices/ Get All Offices
GET /offices/{office_id} Get Office
PUT /offices/{office_id} Update Office
DELETE /offices/{office_id} Delete Office
POST /offices/new Create Office
