---
title: Метод WSMan. Жетеррормессаже (Всмандисп. h)
description: Возвращает отформатированную строку, содержащую текст номера ошибки.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода жетеррормессаже
- служба удаленного управления Windows метода жетеррормессаже, объект WSMan
- объект WSMan служба удаленного управления Windows, метод жетеррормессаже
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e7f23a5d2678d3df024c78397aaeb6a388d8b75368f329867f6457b9ad4d84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742094"
---
# <a name="wsmangeterrormessage-method"></a>Метод WSMan. Жетеррормессаже

Возвращает отформатированную строку, содержащую текст номера ошибки. Этот метод выполняет ту же операцию, что **и в командной строке** WinRM ( **WinRM helpmsg** ) с *десятичным или шестнадцатеричным номером ошибки*.

## <a name="syntax"></a>Синтаксис


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*номер ошибки* \[ окне\]
</dt> <dd>

Номер сообщения об ошибке в десятичном или шестнадцатеричном формате от WinRM, WinHTTP или других компонентов операционной системы.

</dd> <dt>

*ErrorMessage* \[ заполняет\]
</dt> <dd>

Строка сообщения об ошибке, отформатированная как сообщения, возвращенные командой **WinRM** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Соответствующий метод C++ — [**ивсманекс:: жетеррормессаже**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> </dl>

 

 





