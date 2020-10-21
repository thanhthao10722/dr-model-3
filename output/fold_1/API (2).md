



# User Management API

## GET /gotecq.user-management/export-profile/{user_id}

- Description: Export user information (pdf)
  
- Response  
```json  
"object"  
```  

## POST /gotecq.user-management:add-user-to-facility/facility/{id}

- Description: Add user to facility
  
- Payload  
```json  
{"user": ["string"], "role": ["string"]}  
```

## POST /gotecq.user-management:remove-user-from-facility/facility/{id}

- Description: Remove user out of facility
  
- Payload  
```json  
{"user_id": "string"}  
```
## POST /gotecq.user-management:activate-user-role/facility/{id}

- Description: Activate user's role of facility
  
- Payload  
```json  
{"user_id": "string", "role_id": "string"}  
```  

## POST /gotecq.user-management:deactivate-user-role/facility/{id}

- Description: Deactivate user's role of facility
  
- Payload  
```json  
{"user_id": "string", "role_id": "string"}  
```  

## POST /gotecq.user-management:create-group/group

- Description: Create new group
  
- Payload  
```json  
{"name": "string", "description": "string"}  
```  

## POST /gotecq.user-management:update-group/group/{id}

- Description: Update group
  
- Payload  
```json  
{"name": "string", "description": "string"}  
```  

## POST /gotecq.user-management:delete-group/group/{id}

- Description: Delete group

## POST /gotecq.user-management:create-role/facility/{id}

- Description: Create a new role
  
- Payload  
```json  
{"name": "string", "description": "string", "permission": ["string"]}  
```  

## POST /gotecq.user-management:update-role/facility/{id}

- Description: Update role
  
- Payload  
```json  
{"name": "string", "description": "string", "permission": ["string"], "_iid": "string"}  
```  

## POST /gotecq.user-management:delete-role/facility/{id}

- Description: Delete role
  
- Payload  
```json  
{"_iid": "string"}  
```  

## POST /gotecq.user-management:activate-role/facility/{id}

- Description: Activate role
  
- Payload  
```json  
{"_iid": "string"}  
```  

## POST /gotecq.user-management:deactivate-role/facility/{id}

- Description: Deactivate role
  
- Payload  
```json  
{"_iid": "string"}  
```  

## POST /gotecq.user-management:create-user/user

- Description: Create new user
  
- Payload  
```json  
{"name__prefix": "string", "name__given": "string", "name__family": "string", "name__suffix": "string", "name__middle": "string", "telecom__email": "string", "telecom__phone": "string", "telecom__fax": "string", "language": ["string"], "birthdate": "string", "gender": "string", "address__line": "string", "address__city": "string", "address__state": "string", "address__postal": "string", "address__country": "string", "username": "string", "tags": ["string"]}  
```  

## POST /gotecq.user-management:update-user/user/{id}

- Description: Update user
  
- Payload  
```json  
{"name__prefix": "string", "name__given": "string", "name__family": "string", "name__suffix": "string", "name__middle": "string", "telecom__email": "string", "telecom__phone": "string", "telecom__fax": "string", "language": ["string"], "birthdate": "string", "gender": "string", "address__line": "string", "address__city": "string", "address__state": "string", "address__postal": "string", "address__country": "string", "tags": ["string"], "last_login_time": "string"}  
```  

## POST /gotecq.user-management:delete-user/user/{id}

- Description: Delete user

## POST /gotecq.user-management:send-action/user/{id}

- Description: Send action
  
- Payload  
```json  
{"actions": ["string"]}  
```  

## POST /gotecq.user-management:activate-user/user/{id}

- Description: Activate user

## POST /gotecq.user-management:deactivate-user/user/{id}

- Description: Deactivate user

## POST /gotecq.user-management:sync-user-data/user

- Description: Sync user data with keycloak
  
- Payload  
```json  
{"upstream_user_id": "string", "action": "string"}  
```  

## POST /gotecq.user-management:add-user-to-group/user/{id}

- Description: Add user to groups
  
- Payload  
```json  
{"group": ["string"]}  
```  

## POST /gotecq.user-management:remove-user-from-group/user/{id}

- Description: Remove user from group
  
- Payload  
```json  
{"group_id": "string"}  
```  

## POST /gotecq.user-management:sync-user-timeline/user

- Description: Sync user activity with keycloak

## POST /gotecq.user-management:upload-avatar/user/{id}

- Description: Upload user avatar
  
- Payload  
```json  
{"file": "string"}  
```  

## GET /gotecq.user-management/user

- Description: Get user (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "active": "string", "address__city": "string", "address__country": "string", "address__line": "string", "address__postal": "string", "address__state": "string", "avatar_file_id": "string", "birthdate": "string", "expiration_date": "string", "gender": "string", "language": ["string"], "last_login": "string", "name__family": "string", "name__given": "string", "name__middle": "string", "name__prefix": "string", "name__suffix": "string", "pending_action": [{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_iid": "string", "_updated": "string", "code": "string", "name": "string", "user_id": "string"}], "realm": "string", "tags": ["string"], "telecom__email": "string", "telecom__fax": "string", "telecom__phone": "string", "two_factor_authentication": "string", "upstream_user_id": "string", "username": "string", "verified_email": "string"}]  
```  

## GET /gotecq.user-management/user/{id}

- Description: Get user (item view)
  
- Response  
```json  
{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "active": "string", "address__city": "string", "address__country": "string", "address__line": "string", "address__postal": "string", "address__state": "string", "avatar_file_id": "string", "birthdate": "string", "expiration_date": "string", "gender": "string", "language": ["string"], "last_login": "string", "name__family": "string", "name__given": "string", "name__middle": "string", "name__prefix": "string", "name__suffix": "string", "pending_action": [{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_iid": "string", "_updated": "string", "code": "string", "name": "string", "user_id": "string"}], "realm": "string", "tags": ["string"], "telecom__email": "string", "telecom__fax": "string", "telecom__phone": "string", "two_factor_authentication": "string", "upstream_user_id": "string", "username": "string", "verified_email": "string"}  
```  

## GET /gotecq.user-management/user-summary/{id}

- Description: User summary view (item view)
  
- Response  
```json  
{"facility_count": "string", "group_count": "string", "user_id": "string"}  
```  

## GET /gotecq.user-management/user/{user_id}/facility

- Description: List all facility's id user joins (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "active": "string", "address__city": "string", "address__country": "string", "address__county": "string", "address__line": "string", "address__location": "string", "address__postal": "string", "address__state": "string", "name": "string", "role_count": "string", "tax_id": "string", "telecom__email": "string", "telecom__fax": "string", "telecom__phone": "string", "user_id": "string", "website": "string"}]  
```  

## GET /gotecq.user-management/user/{user_id}/group

- Description: Get groups that user joins (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "description": "string", "name": "string"}]  
```  

## GET /gotecq.user-management/user/{user_id}/not-in-group

- Description: Get groups that user joins (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "description": "string", "name": "string"}]  
```  

## GET /gotecq.user-management/user/{user_id}/{facility_id}/role

- Description: Get all roles of user in facility (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_did": "string", "_etag": "string", "_id": "string", "_iid": "string", "_updated": "string", "active": "string", "description": "string", "facility_id": "string", "name": "string", "permission": [{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "code": "string", "description": "string", "display": "string"}]}]  
```  

## GET /gotecq.user-management/user-action

- Description: Get available user action (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "code": "string", "display": "string"}]  
```  

## GET /gotecq.user-management/user-timeline/{user_id}

- Description: Get user timeline (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "activity": "string", "actor_id": "string", "actor_resource": "string", "description": "string", "end_date": "string", "start_date": "string", "status": "string", "target_id": "string", "target_resource": "string", "type": "string", "upstream_user_id": "string"}]  
```  

## GET /gotecq.user-management/user-activity-type

- Description: Get list of available activity types (resource view)
  
- Response  
```json  
[{"code": "string", "description": "string", "kind": "string", "name": "string"}]  
```  

## GET /gotecq.user-management/permission

- Description: Get available permissions (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "code": "string", "description": "string", "display": "string"}]  
```  

## GET /gotecq.user-management/group

- Description: Get group (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "description": "string", "name": "string"}]  
```  

## GET /gotecq.user-management/group/{id}

- Description: Get group (item view)
  
- Response  
```json  
{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "description": "string", "name": "string"}  
```  

## GET /gotecq.user-management/group-summary/{id}

- Description: Get group summary (item view)
  
- Response  
```json  
{"group_id": "string", "user_count": "string"}  
```  

## GET /gotecq.user-management/facility

- Description: Get facility (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "active": "string", "address__city": "string", "address__country": "string", "address__county": "string", "address__line": "string", "address__location": "string", "address__postal": "string", "address__state": "string", "name": "string", "tax_id": "string", "telecom__email": "string", "telecom__fax": "string", "telecom__phone": "string", "website": "string"}]  
```  

## GET /gotecq.user-management/facility/{id}

- Description: Get facility (item view)
  
- Response  
```json  
{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "active": "string", "address__city": "string", "address__country": "string", "address__county": "string", "address__line": "string", "address__location": "string", "address__postal": "string", "address__state": "string", "name": "string", "tax_id": "string", "telecom__email": "string", "telecom__fax": "string", "telecom__phone": "string", "website": "string"}  
```  

## GET /gotecq.user-management/facility-summary/{id}

- Description: Get facility summary (item view)
  
- Response  
```json  
{"facility_id": "string", "user_count": "string"}  
```  

## GET /gotecq.user-management/facility/{facility_id}/role

- Description: Get all roles in facility (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_did": "string", "_etag": "string", "_id": "string", "_iid": "string", "_updated": "string", "active": "string", "description": "string", "facility_id": "string", "name": "string", "permission": [{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "code": "string", "description": "string", "display": "string"}]}]  
```  

## GET /gotecq.user-management/facility/{facility_id}/role/{id}

- Description: Get all roles in facility (item view)
  
- Response  
```json  
{"_created": "string", "_creator": "string", "_deleted": "string", "_did": "string", "_etag": "string", "_id": "string", "_iid": "string", "_updated": "string", "active": "string", "description": "string", "facility_id": "string", "name": "string", "permission": [{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "code": "string", "description": "string", "display": "string"}]}  
```  

## GET /gotecq.user-management/facility/{facility_id}/not-member

- Description: Get all users in facility (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_updated": "string", "active": "string", "address__city": "string", "address__country": "string", "address__line": "string", "address__postal": "string", "address__state": "string", "avatar_file_id": "string", "birthdate": "string", "expiration_date": "string", "gender": "string", "language": ["string"], "last_login": "string", "name__family": "string", "name__given": "string", "name__middle": "string", "name__prefix": "string", "name__suffix": "string", "pending_action": [{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_id": "string", "_iid": "string", "_updated": "string", "code": "string", "name": "string", "user_id": "string"}], "realm": "string", "tags": ["string"], "telecom__email": "string", "telecom__fax": "string", "telecom__phone": "string", "two_factor_authentication": "string", "upstream_user_id": "string", "username": "string", "verified_email": "string"}]  
```  

## GET /gotecq.user-management/facility/{facility_id}/member

- Description: Get all users in facility (resource view)
  
- Response  
```json  
[{"_created": "string", "_creator": "string", "_deleted": "string", "_etag": "string", "_updated": "string", "role_count": "string", "user_id": "string"}]  
```  

## GET /gotecq.user-management/overview-dashboard

- Description: Get dashboard overview information (resource view)
  
- Response  
```json  
[{"total_active_facility": "string", "total_active_user": "string", "total_deactive_facility": "string", "total_deactive_user": "string", "total_facility": "string", "total_group": "string", "total_user": "string"}]  
```  

## GET /gotecq.user-management/user-statistic

- Description: Get dashboard user statistic (resource view)
  
- Response  
```json  
[{"date_effective": "string", "total_facility": "string", "total_user": "string"}]  
```  

## GET /gotecq.user-management/facility-city

- Description: Get list of available cities (resource view)
  
- Response  
```json  
[{"name": "string"}]  
```  

## GET /gotecq.user-management/facility-state

- Description: Get list of available states (resource view)
  
- Response  
```json  
[{"name": "string"}]  
```  

## GET /gotecq.user-management/tag

- Description: Get list of available tags (resource view)
  
- Response  
```json  
[{"description": "string", "kind": "string", "name": "string"}]  
```  
