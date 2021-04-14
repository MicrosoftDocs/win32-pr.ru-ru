---
description: Флаги D3DXSHADER используются для синтаксического анализа, компиляции или сборки шейдеров.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: Флаги D3DXSHADER (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_PACKMATRIX_COLUMNMAJOR
- D3DXSHADER_PACKMATRIX_ROWMAJOR
- D3DXSHADER_AVOID_FLOW_CONTROL
- D3DXSHADER_DEBUG
- D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_IEEE_STRICTNESS
- D3DXSHADER_NO_PRESHADER
- D3DXSHADER_OPTIMIZATION_LEVEL0
- D3DXSHADER_OPTIMIZATION_LEVEL1
- D3DXSHADER_OPTIMIZATION_LEVEL2
- D3DXSHADER_OPTIMIZATION_LEVEL3
- D3DXSHADER_PARTIALPRECISION
- D3DXSHADER_PREFER_FLOW_CONTROL
- D3DXSHADER_SKIPOPTIMIZATION
- D3DXSHADER_SKIPVALIDATION
- D3DXSHADER_USE_LEGACY_D3DX9_31_DLL
- D3DXSHADER_DEBUG
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_SKIPVALIDATION
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f5d35f8c3bdf556e188c2cab8ff2684449b226f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647839"
---
# <a name="d3dxshader-flags"></a>Флаги D3DXSHADER

Флаги **D3DXSHADER** используются для синтаксического анализа, компиляции или сборки шейдеров.

**Флаги средства синтаксического анализа**

Флаги времени синтаксического анализа используются только системой эффектов (до компиляции эффектов) при создании компилятора эффектов. Например, можно создать объект компилятора с **D3DXSHADER \_ паккматрикс \_ колумнмажор**, а затем многократно использовать этот объект компилятора с различными флагами компилятора для создания специализированного кода.



| Константа                                                                                                                                                                                                                   | Описание                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ паккматрикс \_ колумнмажор**</dt> </dl> | Если явно не указано иное, матрицы будут упаковываться в основной порядок столбцов (каждый вектор будет находиться в одном столбце) при передаче в шейдер и из него. Как правило, это более эффективно, поскольку позволяет выполнять умножение векторных матриц с помощью ряда изделий с точками.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ паккматрикс \_ ровмажор**</dt> </dl>          | Если явно не указано иное, матрицы будут упаковываться в основной порядок (каждый вектор будет находиться в одной строке) при передаче в шейдер или из него.<br/>                                                                                                                                        |



**Флаги компилятора**

Компилятор HLSL DirectX 10 теперь является компилятором по умолчанию. Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .

В следующей таблице приведены флаги, доступные в Direct3D 9 и Direct3D 10. Значение флага является эквивалентным параметром fxc.



| Константа/значение                                                                                                                                                                                                                                                                                                | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ Избегайте \_ /ГФА \_ управления потоком**</dt> <dt></dt> </dl>                                     | Это указание компилятору, чтобы не использовать инструкции управления потоком.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ ОТЛАДКа**</dt> <dt>/Zi</dt> </dl>                                                                               | Вставьте имя файла отладки, Номера строк, сведения о типе и символах во время компиляции шейдера.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ ВКЛЮЧИТЬ \_ обратную \_ Совместимость**</dt> <dt>/жек</dt> </dl> | Скомпилируйте \_ \_ шейдеры PS 1 x как PS \_ 2 \_ 0. Эффекты, указывающие \_ \_ целевые объекты PS 1 x, будут компилироваться в \_ \_ целевые объекты PS 2 0, так как это минимальная версия шейдера, поддерживаемая версией компилятора шейдеров, поставляемой с DirectX 10. Этот флаг не оказывает влияния при использовании целевых объектов компиляции более высокого уровня.<br/> Direct3D 9 — нет<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ ПРИНУДИТЕЛЬное \_ \_ программное обеспечение PS \_ НУПТ**</dt> <dt>N/A</dt> </dl>                      | Заставить компилятор компилироваться со следующей самой высокой доступной программной целью для шейдеров пикселей. Этот флаг также отключает оптимизацию и отладку в.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ ПРИНУДИТЕЛЬно использовать \_ \_ программное обеспечение VS \_ НУПТ**</dt> <dt>N/A</dt> </dl>                      | Запустите компилятор для компиляции со следующей самой высокой доступной программной целью для шейдеров вершин. Этот флаг также отключает оптимизацию и отладку в.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ \_**</dt> <dt>/Гисность</dt> IEEE </dl>                                               | Отключите оптимизацию, которая может привести к тому, что выходные данные скомпилированной программы шейдера будут отличаться от выходных данных программы, скомпилированной с помощью компилятора шейдера DirectX 9, из-за небольшого числа opravě в математических вычислениях с плавающей запятой.<br/> Direct3D 9 — нет<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ НЕТ \_ ПРЕДшейдера**</dt> <dt>/Op</dt> </dl>                                                         | Отключает предшейдеры. Компилятор не будет запрашивать статические выражения для вычисления на центральном процессоре узла. Кроме того, компилятор не будет лофт никаких выражений при компиляции изолированных функций.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ Оптимизация \_ LEVEL0**</dt> <dt>/O0</dt> </dl>                                    | Минимальный уровень оптимизации. Может создать более медленный код, но сделает это быстрее. Это может быть полезно в цикле разработки высокоитеративного шейдера.<br/> Direct3D 9 — нет<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ Оптимизация \_ level1**</dt> <dt>/O1</dt> </dl>                                    | Второй самый низкий уровень оптимизации.<br/> Direct3D 9 — нет<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ Оптимизация \_ level2**</dt> <dt>/O2</dt> </dl>                                    | Второй высший уровень оптимизации.<br/> Direct3D 9 — нет<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ Оптимизация \_ LEVEL3**</dt> <dt>/O3</dt> </dl>                                    | Наивысший уровень оптимизации. Выдаст лучшие возможности кода, но это может занять значительно больше времени. Это будет полезно для финальных сборок приложения, где производительность является наиболее важным фактором.<br/> Direct3D 9 — нет<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ ПАРТИАЛПРЕЦИСИОН**</dt> <dt>/ГПП</dt> </dl>                                             | Принудительно выполнять все вычисления в результирующем шейдере с частичной точностью. Это может привести к более быстрой оценке шейдеров на некоторых устройствах.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ ПРЕДПОЧИТАТЬ \_ /GFP \_ управления потоком**</dt> <dt></dt> </dl>                                  | Это указание компилятору, которое предпочитает использовать инструкции управления потоком.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ СКИПОПТИМИЗАТИОН**</dt> <dt>/OD</dt> </dl>                                              | Попросите компилятора пропустить шаги оптимизации во время создания кода. Если вы не пытаетесь изолировать проблему в коде и вы подозреваете компилятор, использовать этот параметр не рекомендуется.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ СКИПВАЛИДАТИОН**</dt> <dt>/ВД</dt> </dl>                                                    | Не проверяйте созданный код на соответствие известным возможностям и ограничениям. Этот параметр рекомендуется использовать только при компиляции известных шейдеров (то есть шейдеров, скомпилированных ранее без этого параметра). Шейдер всегда проверяется средой выполнения до того, как они задаются для устройства.<br/> Direct3D 9 — Да<br/> Direct3D 10 — да<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ ИСПОЛЬЗОВАТЬ \_ устаревшую \_ \_ \_ библиотеку DLL/LD D3DX9 31**</dt> <dt></dt> </dl>                     | Включите использование исходного компилятора Direct3D 9 HLSL. OCT2006 \_ d3dx9 \_ 31 \_x86.cab или OCT2006 \_ d3dx9 \_ 31 \_x64.cab должны быть включены в состав распространяемых приложений. Этот флаг необходим для компиляции \_ \_ шейдеров PS 1 x без использования флага повышения уровня для PS \_ 2 \_ 0. Указание этого флага при получении интерфейса [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) приводит к последующим вызовам [**компилиффект**](id3dxeffectcompiler--compileeffect.md) и [**компилешадер**](id3dxeffectcompiler--compileshader.md) через этот объект, чтобы использовать устаревший компилятор.<br/> Direct3D 9 — Да<br/> Direct3D 10 — нет<br/> |



**Флаги ассемблера**

Флаги ассемблера используются системой эффектов для оптимизации шейдера и повлиять на код сборки.



| Константа                                                                                                                                                                                                                        | Описание                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**\_Отладка D3DXSHADER**</dt> </dl>                                                          | Вставьте имя файла отладки, Номера строк, сведения о типе и символах во время компиляции шейдера.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ \_ НУПТ Software \_**</dt> </dl> | Заставить компилятор компилироваться со следующей самой высокой доступной программной целью для шейдеров пикселей. Этот флаг также отключает оптимизацию и отладку в.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ VS \_ Software \_ НУПТ**</dt> </dl> | Запустите компилятор для компиляции со следующей самой высокой доступной программной целью для шейдеров вершин. Этот флаг также отключает оптимизацию и отладку в.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ скипвалидатион**</dt> </dl>                               | Не проверяйте созданный код на соответствие известным возможностям и ограничениям. Этот параметр рекомендуется использовать только при компиляции известных шейдеров (то есть шейдеров, скомпилированных ранее без этого параметра). Шейдер всегда проверяется средой выполнения до того, как они задаются для устройства.<br/> |



## <a name="remarks"></a>Комментарии

Система эффектов будет использовать **Флаги синтаксического анализатора** при вызове следующими функциями:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**компилиффект**](id3dxeffectcompiler--compileeffect.md)

Система эффектов будет использовать **флаги компилятора** при вызове следующих функций:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (или [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) или [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**Компилиффект**](id3dxeffectcompiler--compileeffect.md) (или [**компилешадер**](id3dxeffectcompiler--compileshader.md))

Кроме того, можно использовать **флаги компилятора** при создании эффектов путем вызова [**D3DXCreateEffect**](d3dxcreateeffect.md) (или [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) или [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)).

-   При передаче некомпилированного файла. FX система эффектов будет использовать входной параметр флага во время компиляции.
-   При передаче скомпилированного результата система эффектов будет игнорировать флаги компилятора, так как они не нужны для загрузки результата.

Система эффектов будет использовать **Флаги ассемблера** при вызове следующими функциями:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

Применение **флагов компилятора** или **флагов ассемблера** к неверному API приведет к сбою проверки шейдера. Проверьте возвращаемое значение кода ошибки Direct3D в функции с помощью средства поиска ошибок DirectX (DXErr.exe), чтобы устранить эту ошибку. Вы можете получить DXErr.exe и узнать о нем из пакета SDK DirectX. Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
