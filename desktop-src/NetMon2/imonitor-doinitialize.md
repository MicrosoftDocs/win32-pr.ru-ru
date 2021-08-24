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
ms.openlocfilehash: 013a1604c1cbc709f35ac23378bab008d6c67f9053c171190b20669106303f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779184"
---
# <a name="imonitordoinitialize-method"></a>Имонитор: метод:D Оинитиализе

Метод **доинитиализе** должен быть реализован монитором. мксвк вызывает этот метод для получения фильтра записи непосредственно перед вызовом метода [иртк:: Подключение](irtc-connect.md) нпп.

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

## <a name="remarks"></a>Remarks

МКСВК вызывает метод **доинитиализе** для выполнения любой необходимой инициализации монитора.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

