---
title: Метод SendMessage класса Win32_VirtualDesktopSession
description: Отправка сообщения пользователю через сеанс виртуального рабочего стола.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Метод SendMessage службы удаленных рабочих столов
- Метод SendMessage службы удаленных рабочих столов, Win32_VirtualDesktopSession класс
- Win32_VirtualDesktopSession службы удаленных рабочих столов класса, метод SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415448"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>Метод SendMessage \_ класса Win32 виртуалдесктопсессион

Отправка сообщения пользователю через сеанс виртуального рабочего стола.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Название* \[ окне\]
</dt> <dd>

Заголовок сообщений.

</dd> <dt>

*Сообщение об ошибке* \[ окне\]
</dt> <dd>

Содержимое сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Виртуалдесктопсессион Win32**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





