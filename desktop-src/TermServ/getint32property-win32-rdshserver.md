---
title: Метод GetInt32Property класса Win32_RDSHServer (Microsoft. Diagnostics. аппаналисис. h)
description: Извлекает значение целочисленного свойства \_ объекта Рдшсервер Win32.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода GetInt32Property
- Службы удаленных рабочих столов метода GetInt32Property, класс Win32_RDSHServer
- Класс Win32_RDSHServer службы удаленных рабочих столов, метод GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9114ca22a1052161000fcb05f38622ab9d210ec02b14715dad1bb85ce1365e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130675"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a>Метод GetInt32Property \_ класса Win32 рдшсервер

Извлекает значение целочисленного свойства объекта [**\_ рдшсервер Win32**](win32-rdshserver.md) .

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Ключ, определяющий извлекаемое свойство.

</dd> <dt>

*Значение* \[ заполняет\]
</dt> <dd>

Получает полученное значение свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                                 |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                                   |
| Заголовок<br/>                   | <dl> <dt>Microsoft. Diagnostics. аппаналисис. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Рдшсервер Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





