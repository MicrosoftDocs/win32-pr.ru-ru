---
description: Извлекает массив байтов, содержащий данные внутреннего свойства и внутренних свойств для данного Иконтекстноде.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'Метод Иконтекстноде:: Савепропертиесдата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5b02f5df7526b429a65b2a0baf49bda4571dd718a9bff875c79b7e325de244ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719688"
---
# <a name="icontextnodesavepropertiesdata-method"></a>Метод Иконтекстноде:: Савепропертиесдата

Извлекает массив байтов, содержащий данные внутреннего свойства и внутренних свойств для данного [**иконтекстноде**](icontextnode.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулпропертиесдатасизе* \[ в, out\]
</dt> <dd>

Размер массива данных, содержащего сведения о свойстве. Переданное значение не используется.

</dd> <dt>

*ппбпропертиесдата* \[ заполняет\]
</dt> <dd>

Указатель на массив 8-разрядных целых чисел без знака, который содержит данные свойства и внутренних свойств для конкретного приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппбпропертиесдата* , если эта информация больше не нужна.

 

Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Этот метод сохраняет данные свойства, установленные **иинканализер** в [**иконтекстноде**](icontextnode.md).

Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Лоадпропертиесдата**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Иконтекстноде:: Аддпропертидата**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Ремовепропертидата**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидатаидс**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Иконтекстноде:: Контаинспропертидата**](icontextnode-containspropertydata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

