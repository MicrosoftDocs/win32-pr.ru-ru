---
title: Функция Мпманажерверсионкуери (Мпклиент. h)
description: Возвращает сведения о версии различных компонентов диспетчера защиты от вредоносных программ.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- функции мпманажерверсионкуери устаревших функций среды Windows
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6407f36650b699f6bcdc9cbdd832ff2db38f68e9db758411d42aa5e81564ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114544"
---
# <a name="mpmanagerversionquery-function"></a>Функция Мпманажерверсионкуери

Возвращает сведения о версии различных компонентов диспетчера защиты от вредоносных программ.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмфандле* \[ окне\]
</dt> <dd>

Тип: **мфандле**

Обработчик для интерфейса диспетчера защиты от вредоносных программ. Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .

</dd> <dt>

*пверсионинфо* \[ заполняет\]
</dt> <dd>

Тип: **пмпверсион \_ info** .

Указатель на структуру, содержащую сведения о версии различных компонентов диспетчера защиты от вредоносных программ. См [**. \_ сведения о MPVERSION**](mpversion-info.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если функция выполнена успешно, возвращается значение **S \_**.

Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** . Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мперрормессажеформат**](mperrormessageformat.md)
</dt> <dt>

[**мпманажеропен**](mpmanageropen.md)
</dt> <dt>

[**\_сведения о MPVERSION**](mpversion-info.md)
</dt> </dl>

 

 





