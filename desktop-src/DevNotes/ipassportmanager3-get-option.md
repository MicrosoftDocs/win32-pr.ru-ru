---
description: Получает значение конкретного параметра входа Microsoft .NET Passport.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'Метод IPassportManager3:: get_Option'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423198"
---
# <a name="ipassportmanager3get_option-method"></a>Метод IPassportManager3:: Get \_

Получает значение конкретного параметра входа Microsoft .NET Passport.

> [!Note]  
> Метод **получения \_ параметра** принадлежит интерфейсу [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Этот раздел дополняет исходную документацию.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя* \[ окне\]
</dt> <dd>

Возвращаемый параметр входа. В настоящее время поддерживается только параметр "Имоде".

</dd> <dt>

*Pval* \[ заполняет\]
</dt> <dd>

Указатель на **вариант Variant (тип** \_ bool), который получает значение параметра. Это значение может быть true или false.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении метода возвращает значение ОК.

## <a name="remarks"></a>Комментарии

Этот метод поставляется со старыми версиями пакета SDK для Passport.

 

 
