---
title: Метод повторного подключения IMsRdpClient8
description: Повторно подключается к удаленному сеансу, используя новые значения ширины и высоты рабочего стола.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода повторного подключения
- Службы удаленных рабочих столов метода повторного подключения, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Reconnect
- Службы удаленных рабочих столов метода повторного подключения, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Reconnect
- Службы удаленных рабочих столов метода повторного подключения, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Reconnect
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535585"
---
# <a name="imsrdpclient8reconnect-method"></a>Метод IMsRdpClient8:: Reconnect

Повторно подключается к удаленному сеансу, используя новые значения ширины и высоты рабочего стола. Чтобы этот метод был выполнен, элемент управления уже должен быть подключен к удаленному сеансу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улвидс* \[ окне\]
</dt> <dd>

Тип: **ulong**

Новая ширина рабочего стола в пикселях. См. свойство [**десктопвидс**](imstscax-desktopwidth.md) для ограничений по значению.

</dd> <dt>

*улхеигхт* \[ окне\]
</dt> <dd>

Тип: **ulong**

Новая высота рабочего стола (в пикселях). См. свойство [**десктофеигхт**](imstscax-desktopheight.md) для ограничений по значению.

</dd> <dt>

*преконнектстатус* \[ out, retval\]
</dt> <dd>

Тип: **[**контролреконнектстатус**](controlreconnectstatus.md) \** _

Указатель на переменную [_ *контролреконнектстатус* *](controlreconnectstatus.md) , которая получает состояние операции повторного соединения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 определен как 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**контролреконнектстатус**](controlreconnectstatus.md)
</dt> </dl>

 

 





