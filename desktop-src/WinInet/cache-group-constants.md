---
title: Константы группы кэша (WinInet. h)
description: В следующем списке содержатся константы, используемые функциями группы кэша.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb79ae76d743ff4633f6d7f359f96906d2f60cc64c2c35ab2544ae80918721a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955624"
---
# <a name="cache-group-constants"></a>Константы группы кэша

В следующем списке содержатся константы, используемые функциями группы кэша.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**\_атрибут качеграуп \_ Basic**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Извлекает атрибуты флага, типа и дисковой квоты группы кэша. Это используется функцией [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_флаг атрибута \_ качеграуп**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Задает или получает флаги, связанные с группой кэша. Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**КАЧЕГРАУП \_ атрибут \_ Get \_**
</dt> <dd> <dl> <dt>

0xffffffff
</dt> <dt>



Извлекает все атрибуты группы кэша. Это используется функцией [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**КАЧЕГРАУП, \_ атрибут \_ GROUPNAME**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Задает или получает имя группы кэша. Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_ \_ Квота атрибута качеграуп**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Задает или получает дисковую квоту, связанную с группой кэша. Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_хранилище АТРИБУТОВ \_ качеграуп**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Задает или получает хранилище владельца группы, связанное с группой кэша. Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_тип атрибута \_ качеграуп**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Задает или получает тип группы кэша. Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**КАЧЕГРАУП \_ \_ ФЛУШУРЛ, \_ Удаление флага**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Указывает, что все записи кэша, связанные с группой кэша, должны быть удалены, если только запись не принадлежит другой группе кэша.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**\_гидонли флаг \_ качеграуп**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Указывает, что функция должна создавать только уникальный идентификатор GROUPID для группы кэша и не создавать фактическую группу.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**Флаг КАЧЕГРАУП не был \_ \_ очищен**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Указывает, что группа кэша не может быть очищена.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_Маска качеграуп ReadWrite \_**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Задает тип, квоту диска, имя группы и атрибуты хранилища владельца группы кэша. Это используется функцией [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**КАЧЕГРАУП \_ Поиск \_ всех**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Указывает, что необходимо перечислить все группы кэша в системе пользователя.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**КАЧЕГРАУП \_ поиска \_ бюрл**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



В настоящий момент не реализовано.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**\_Недопустимый тип качеграуп \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Указывает, что тип группы кэша недопустим.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_ \_ Размер хранилища владельца \_ группы**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Длина массива хранения владельца группы.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**ИМЯ_ГРУППЫ \_ Максимальная \_ Длина**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Максимальное число символов, разрешенное для имени группы кэша.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

