---
description: Задает конкретный параметр входа Microsoft .NET Passport.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: 'IPassportManager3: метод ut_Option:p'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92a1c432df3f3948a85205e26da64073722ba84dd365ebdcaccf3b80521c517c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827238"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3::p \_ метод параметра UT

Задает конкретный параметр входа Microsoft .NET Passport.

> [!Note]  
> Метод **\_ варианта размещения** принадлежит интерфейсу [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Этот раздел дополняет исходную документацию.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*name* 
</dt> <dd>

Параметр входа для установки. В настоящее время единственным поддерживаемым параметром является Имоде.

</dd> <dt>

*неввал* 
</dt> <dd>

**Вариант Variant** ( \_ логическое значение VT), указывающий новый параметр. Это значение может быть true или false.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении метода возвращает значение ОК.

## <a name="remarks"></a>Remarks

Этот метод поставляется со старыми версиями пакета SDK для Passport.

 

 
