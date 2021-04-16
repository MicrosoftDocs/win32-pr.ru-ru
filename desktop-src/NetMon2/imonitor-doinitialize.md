---
description: Метод Доинитиализе должен быть реализован монитором. МКСВК вызывает этот метод для получения фильтра записи непосредственно перед вызовом метода НППС Ирткконнект.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Метод Имонитордоинитиализе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540178"
---
# <a name="imonitordoinitialize-method"></a>Имонитор: метод:D Оинитиализе

Метод **доинитиализе** должен быть реализован монитором. МКСВК вызывает этот метод для получения фильтра записи непосредственно перед вызовом метода [ИРТК:: Connect](irtc-connect.md) НПП.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пункмониторктрл* \[ окне\]
</dt> <dd>

Указатель [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , переданный мксвк. Чтобы получить поддерживаемый интерфейс управления монитором, монитор должен вызвать метод [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе.

</dd> <dt>

*хнппблоб* \[ в, out\]
</dt> <dd>

На входе — маркер для большого двоичного объекта НПП.

На выходе — большой двоичный объект НПП, содержащий фильтр записи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ OK (то же самое, что и ошибка).

Если метод завершается неудачно, возвращаемое значение является кодом ошибки. При возникновении ошибки МКСВК не создаст монитор или вызовите метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) на указатель интерфейса.

## <a name="remarks"></a>Комментарии

МКСВК вызывает метод **доинитиализе** для выполнения любой необходимой инициализации монитора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

