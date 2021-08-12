---
title: IDXCoreAdapterList::Sort
description: Сортирует объект списка адаптеров Дкскоре на основе предоставленного входного массива критериев сортировки.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 59580fb8b76c80a264796f829d2b0a1d2e8eabb4375896fbd27fb34a7697cf90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278875"
---
# <a name="idxcoreadapterlistsort-method"></a>Метод Идкскореадаптерлист:: Sort

## <a name="description"></a>Описание

Сортирует объект списка адаптеров Дкскоре на основе предоставленного входного массива критериев сортировки, где элементы массива ранее в массиве критериев имеют более высокий вес. **Сортировка** помогает легко найти идеальный адаптер в списке адаптеров.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>Параметры

### <a name="numpreferences"></a>нумпреференцес

Тип: **uint32_t**

Количество элементов в массиве, на которое указывает параметр *Preferences* .

### <a name="preferences-in"></a>предпочтения [в]

Тип: **const [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Указатель на константный массив значений [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) , представляющих критерий сортировки.

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|E_INVALIDARG|Аргумент *нумпреференцес* равен нулю, либо аргументу *Preferences* является `nullptr` .|

## <a name="remarks"></a>Remarks

В случаях, когда указанное значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) не распознается операционной системой (ОС), оно игнорируется и не приводит к сбою API. Известные значения **дкскореадаптерпреференце** по-прежнему будут учитываться в этом случае. Чтобы определить, понят ли тип сортировки для API, вызовите метод [идкскореадаптерлист:: исадаптерпреференцесуппортед](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

Значения **дкскореадаптерпреференце** , которые происходят ранее в предоставленном массиве *предпочтений* , обрабатываются с более высоким приоритетом. 

Дополнительные сведения о том, какая логика применяется к каждому типу, см. в документации по перечислению **дкскореадаптерпреференце** . Внутренняя логика типа может разрабатываться по мере разработки ОС.

При **сортировке** элементы списка адаптеров дкскоре будут отсортированы от наиболее предпочтительных до наименьшего. Таким образом, вызов [идкскореадаптерлист:: Adapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) с индексом 0 получает адаптер, который наилучшим образом соответствует запрошенным типам предпочтений сортировки. индекс 1 — это следующее лучшее соответствие и т. д.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)