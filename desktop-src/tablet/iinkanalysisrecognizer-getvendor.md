---
description: Возвращает имя поставщика Иинканалисисрекогнизер.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: Метод Иинканалисисрекогнизер::-Vendor (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145487"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a>Метод Иинканалисисрекогнизер:: Vendor

Возвращает имя поставщика [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбстрвендор* \[ заполняет\]
</dt> <dd>

Имя поставщика.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для \* *пбстрвендор* , когда больше не нужно использовать строку.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

