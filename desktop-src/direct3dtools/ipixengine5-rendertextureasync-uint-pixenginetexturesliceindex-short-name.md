---
description: Визуализирует текстуру в файл и возвращает результат в асинчрнаусли узла.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Рендертекстуреасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400ade8aa962a73234efbfb710d9ab6b178dfd4e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626570"
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
