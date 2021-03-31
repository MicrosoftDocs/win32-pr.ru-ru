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
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071551"
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**имсрдпворкспаце**](imsrdpworkspace.md)
</dt> </dl>

 

