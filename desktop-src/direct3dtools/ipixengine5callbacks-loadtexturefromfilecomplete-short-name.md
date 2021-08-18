---
description: Функция обратного вызова, используемая для уведомления узла о завершении загрузки текстуры.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5Callbacks:: Лоадтекстурефромфилекомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e9a9530fb9ada600d818494565765655c2c8cfb3bca938d8b9dff9d240aa6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985974"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>Метод IPixEngine5Callbacks:: Лоадтекстурефромфилекомплете

Функция обратного вызова, используемая для уведомления узла о завершении загрузки текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a>Параметры

*текстуреид*   
Идентификатор загруженной текстуры.

*текстуредеск*   
Дескриптор текстуры загруженной текстуры.

*нумслицес*   
Число срезов, которые имеет текстура.

*count2 \_ слицеиндиЦиес*   
Срез индиЦиес, связанный с текстурой.

*count2 \_ слицедескрипторс*   
Дескрипторы для каждого среза.

*нумформатоверридес*   
Число переопределений формата.

*count5 \_ форматоверридес*   
Формат переопределяет.

*отображения*   
Адрес данных гистограммы загруженной текстуры.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
