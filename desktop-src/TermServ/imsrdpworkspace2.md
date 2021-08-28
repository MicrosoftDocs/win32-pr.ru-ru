---
title: Интерфейс IMsRdpWorkspace2
description: Предоставляет метод, связывающий подключения к удаленным рабочим столам и приложениям RemoteApp учетные данные с соединением.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпворкспаце
- Службы удаленных рабочих столов интерфейса Имсрдпворкспаце, описание
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b869d3ffc83d9a4b8f3d51df0b7b14658ec3f1c561797a62dee3a574bf2803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125524"
---
# <a name="imsrdpworkspace2-interface"></a>Интерфейс IMsRdpWorkspace2

Предоставляет метод, связывающий подключения к удаленным рабочим столам и приложениям RemoteApp учетные данные с соединением. Этот интерфейс реализуется элементом управления службы удаленных рабочих столов Веб-доступ. Этот элемент управления является оболочкой для подключение к удаленному рабочему столу клиента (MsTscAx.dll), а также прокси-сервера среды выполнения подключений RemoteApp и Desktop Connections (Tswbprxy.exe).

## <a name="members"></a>Элементы

Интерфейс **имсрдпворкспаце** наследует от [**имсрдпворкспаце**](imsrdpworkspace.md). **IMsRdpWorkspace2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **имсрдпворкспаце** содержит следующие методы.



| Метод                                                        | Описание                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**стартворкспацеекс**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Связывает учетные данные пользователя и сертификаты с ИДЕНТИФИКАТОРом подключения. <br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace2 определен как 145D0622-04CF-4FC3-A776-A82A9169CDF8<br/>           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**имсрдпворкспаце**](imsrdpworkspace.md)
</dt> </dl>

 

