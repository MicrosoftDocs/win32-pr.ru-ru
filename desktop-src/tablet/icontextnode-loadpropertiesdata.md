---
description: 'Повторно создает данные о свойстве и внутренних свойствах приложения для массива байтов, созданного ранее с помощью Иконтекстноде:: Савепропертиесдата.'
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'Метод Иконтекстноде:: Лоадпропертиесдата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692436"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>Метод Иконтекстноде:: Лоадпропертиесдата

Повторно создает данные о свойстве и внутренних свойствах приложения для массива байтов, созданного ранее с помощью [**иконтекстноде:: савепропертиесдата**](icontextnode-savepropertiesdata.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кбпропертиесдатасизе* \[ окне\]
</dt> <dd>

Размер массива данных свойств.

</dd> <dt>

*пбпропертиесдата* \[ окне\]
</dt> <dd>

Массив 8-разрядных целых чисел без знака, содержащий сведения о свойствах для загрузки.

</dd> <dt>

*пфсукцессфул* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если данные свойства успешно загружены; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Аддпропертидата**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Контаинспропертидата**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидатаидс**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Иконтекстноде:: Ремовепропертидата**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Савепропертиесдата**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




