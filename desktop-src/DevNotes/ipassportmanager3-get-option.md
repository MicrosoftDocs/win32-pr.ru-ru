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
ms.openlocfilehash: 5d7260e3c13be21f1cc963e1bca15a6126739a0075b94ee11f07d98901efd39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750044"
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

## <a name="remarks"></a>Remarks

Этот метод поставляется со старыми версиями пакета SDK для Passport.

 

 
