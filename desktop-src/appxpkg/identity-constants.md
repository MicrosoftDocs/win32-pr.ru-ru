---
title: Константы удостоверений (AppModel. h)
description: Задает длину строк для полей идентификаторов пакета.
ms.assetid: C4F81822-B502-4360-AEA4-829F1AB926BF
topic_type:
- apiref
api_name:
- APPLICATION_USER_MODEL_ID_MAX_LENGTH
- APPLICATION_USER_MODEL_ID_MIN_LENGTH
- PACKAGE_ARCHITECTURE_MAX_LENGTH
- PACKAGE_ARCHITECTURE_MIN_LENGTH
- PACKAGE_FAMILY_NAME_MAX_LENGTH
- PACKAGE_FAMILY_NAME_MIN_LENGTH
- PACKAGE_FULL_NAME_MAX_LENGTH
- PACKAGE_FULL_NAME_MIN_LENGTH
- PACKAGE_NAME_MAX_LENGTH
- PACKAGE_NAME_MIN_LENGTH
- PACKAGE_PUBLISHERID_MAX_LENGTH
- PACKAGE_PUBLISHERID_MIN_LENGTH
- PACKAGE_PUBLISHER_MAX_LENGTH
- PACKAGE_PUBLISHER_MIN_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH
- PACKAGE_RESOURCEID_MAX_LENGTH
- PACKAGE_RESOURCEID_MIN_LENGTH
- PACKAGE_VERSION_MAX_LENGTH
- PACKAGE_VERSION_MIN_LENGTH
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4590e62397ac069cb0fc9661f615288c2d8df36ba41304fff71e4ef0293f9f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552216"
---
# <a name="identity-constants"></a>Константы удостоверений

Задает длину строк для полей идентификаторов пакета. Длина измеряется в символах и может содержать или не включать пробел для терминатора NULL.

> [!Note]  
> Константы в формате: **\_ \_ \_ \_ \* \_ Длина идентификатора модели пользователя приложения** и **\_ \_ \_ \_ \* \_ Длина идентификатора приложения, относительная для пакета** , включают пробел для нулевого терминатора, но константы в форме: **\_ \* \_ Длина пакета** не включает пробел для нулевого терминатора.

 



| Константа/значение                                                                                                                                                                                                                                                                                                   | Описание                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**Приложение \_ \_ \_ \_ Максимальная \_ длина идентификатора пользовательской модели**</dt> <dt>130</dt> </dl>                  | Максимальная длина идентификатора модели пользователя приложения. Для терминатора NULL включено пространство.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**Приложение \_ \_ \_ \_ Минимальная \_ Длина идентификатора модели пользователя**</dt> <dt>21</dt> </dl>                   | Минимальная длина идентификатора модели пользователя приложения. Для терминатора NULL включено пространство.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**Пакетная \_ \_Максимальная \_ Длина архитектуры**</dt> <dt>7</dt> </dl>                                     | Максимальная длина архитектуры. Для терминатора NULL не предусмотрено пространство.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**Пакетная \_ \_Минимальная \_ Длина архитектуры**</dt> <dt>3</dt> </dl>                                     | Минимальная длина архитектуры. Для терминатора NULL не предусмотрено пространство.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**Пакетная \_ \_ \_ Максимальная \_ длина имени семейства**</dt> <dt>64</dt> </dl>                                      | Максимальная длина имени семейства. Для терминатора NULL не предусмотрено пространство.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**Пакетная \_ Имя семейства — \_ \_ Минимальная \_ Длина**</dt> <dt>17</dt> </dl>                                      | Минимальная длина имени семейства. Для терминатора NULL не предусмотрено пространство.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**Пакетная \_ \_ \_ Максимальная \_ длина полного имени**</dt> <dt>127</dt> </dl>                                           | Максимальная длина полного имени. Для терминатора NULL не предусмотрено пространство.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**Пакетная \_ ПОЛНОЕ \_ имя \_ min \_ length**</dt> <dt>30</dt> </dl>                                            | Минимальная длина полного имени. Для терминатора NULL не предусмотрено пространство.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**Пакетная \_ \_Максимальная \_ длина имени**</dt> <dt>50</dt> </dl>                                                            | Максимальная длина имени. Для терминатора NULL не предусмотрено пространство.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**Пакетная \_ ИМЯ \_ мин. \_ Длина**</dt> <dt>3</dt> </dl>                                                             | Минимальная длина имени. Для терминатора NULL не предусмотрено пространство.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**Пакетная \_ \_Максимальная \_ Длина PUBLISHERID**</dt> <dt>13</dt> </dl>                                       | Максимальная длина идентификатора издателя. Для терминатора NULL не предусмотрено пространство.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**Пакетная \_ PUBLISHERID \_ Минимальная \_ Длина**</dt> <dt>13</dt> </dl>                                       | Минимальная длина идентификатора издателя. Для терминатора NULL не предусмотрено пространство.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**Пакетная \_ \_Максимальная \_ длина издателя**</dt> <dt>8192</dt> </dl>                                           | Максимальная длина издателя. Например, CN =*Publisher*. Для терминатора NULL не предусмотрено пространство.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**Пакетная \_ \_Минимальная \_ Длина издателя**</dt> ( <dt>4</dt> ) </dl>                                              | Минимальная длина издателя. Для терминатора NULL не предусмотрено пространство.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**Пакетная \_ \_ \_ \_ Максимальная \_ Длина идентификатора приложения**</dt> <dt>65</dt> </dl> | Максимальная длина идентификатора приложения относительно пакета. Для терминатора NULL включено пространство.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**Пакетная \_ \_ \_ \_ \_ Длина идентификатора относительных приложений (мин**</dt> .) <dt>2</dt> </dl>  | Минимальная длина идентификатора приложения относительно пакета. Для терминатора NULL включено пространство.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**Пакетная \_ \_Максимальная \_ Длина RESOURCEID**</dt> , <dt>30</dt> </dl>                                          | Максимальная длина идентификатора ресурса. Для терминатора NULL не предусмотрено пространство.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**Пакетная \_ \_Минимальная \_ Длина RESOURCEID**</dt> <dt>0</dt> </dl>                                           | Минимальная длина идентификатора ресурса. Для терминатора NULL не предусмотрено пространство.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**Пакетная \_ \_Максимальная \_ Длина версии**</dt> <dt>23</dt> </dl>                                                   | Максимальная длина версии. Например, *XXXXX*. *XXXXX*. *XXXXX*. *XXXXX*. Для НУЛЕВого терминатора не предусмотрено пробела/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**Пакетная \_ \_Минимальная \_ Длина версии**</dt> <dt>7</dt> </dl>                                                    | Минимальная длина версии. Например, *x*. *x*. *x*. *x*. Для терминатора NULL не предусмотрено пространство.<br/>                 |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>AppModel. h</dt> </dl> |



 

 





