---
description: Визуализирует текстуру в файл и возвращает результат в асинчрнаусли узла.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Рендертекстуреасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537295"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Рендертекстуреасинк

Визуализирует текстуру в файл и возвращает результат в асинчрнаусли узла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*текстуреид*   
Идентификатор текстуры для отрисовки.

*слицеиндекс*   
Индекс среза в текстуре для отрисовки.

*форматоверриде*   
Переопределение формата цвета.

*сокращение*   

*границ*   

*шадерфиленаме*   
Строка COM, содержащая путь к файлу шейдера.

*нумфлоатшадерварс*   
Число переменных шейдера с плавающей запятой

*count6 \_ шадерфлоатварнаме*   
Строки COM контианинг имена переменных шейдера с плавающей запятой.

*count6 \_ шадерфлоатварвалуе*   
Переменные шейдера с плавающей точкой.

*нумбулшадерварс*   
Число переменных шейдера Boolean.

*count9 \_ шадербулварнаме*   
Строки COM контианинг имена логических переменных шейдера.

*count9 \_ шадербулварвалуе*   
Логические переменные шейдера.

*рендерконтентфиленаме*   
Строка COM, содержащая путь к файлу, в котором была записана подготовленная текстура.

*обратные вызовы*   
Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.

*рекуесткукие*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

*прогрессинтервалмсекс*   
Не используется.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
