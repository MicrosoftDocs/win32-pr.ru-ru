---
title: Метод WSMan. Жетеррормессаже (Всмандисп. h)
description: Возвращает отформатированную строку, содержащую текст номера ошибки.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Жетеррормессаже
- Служба удаленного управления Windows метода Жетеррормессаже, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Жетеррормессаже
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
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340695"
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

## <a name="remarks"></a>Комментарии

Соответствующий метод C++ — [**ивсманекс:: жетеррормессаже**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> </dl>

 

 





