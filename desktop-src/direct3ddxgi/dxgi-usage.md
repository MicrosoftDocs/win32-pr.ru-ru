---
description: Флаги для параметров создания поверхности и ресурсов.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703747"
---
# <a name="dxgi_usage"></a>\_Использование DXGI

Флаги для параметров создания поверхности и ресурсов.



| Константа/значение                                                                                                                                                                                                                                                                                  | Описание                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ 1L \_ использования \_ буфера обмена**</dt> <dt>" << " (2 + 4)</dt> </dl>                             | Поверхность или ресурс используется в качестве заднего буфера. При создании цепочки буферов не нужно передавать **\_ \_ обратную \_ буферизацию использования DXGI** . Но можно определить, принадлежит ли ресурс к цепочке подкачки при вызове [**идксгиресаурце:: Usage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) и получении **\_ \_ обратного \_ буфера использования DXGI**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ \_Отмена использования \_ в \_ настоящее**</dt> время <dt>1L <<  (5 + 4)</dt> </dl>       | Этот флаг предназначен только для внутреннего использования.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ ИСПОЛЬЗОВАНИЕ \_ \_ только для чтения**</dt> <dt> <<  1L (4 + 4)</dt> </dl>                                   | Используйте поверхность или ресурс только для чтения.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ \_Целевой 1L прорисовки \_ \_ данных использования**</dt> <dt> <<  (1 + 4)</dt> </dl> | Используйте область или ресурс в качестве целевого объекта отрисовки выходных данных.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ \_ \_ Входные 1L <<  шейдера использования**</dt> <dt>(0 + 4)</dt> </dl>                          | Используйте поверхность или ресурс в качестве входных данных для шейдера.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ ИСПОЛЬЗОВАНИЕ \_ общего**</dt> <dt>1L <<  (3 + 4)</dt> </dl>                                             | Совместное использование поверхности или ресурса.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ ИСПОЛЬЗОВАНИЕ \_ НЕупорядоченного \_ доступа**</dt> <dt>1L <<  (6 + 4)</dt> </dl>              | Используйте поверхность или ресурс для неупорядоченного доступа.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Комментарии

Каждый флаг определяется как целое число без знака.

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

Эти параметры флага используются при вызове метода [**идксгифактори:: креатесвапчаин**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: креатесвапчаинфорхвнд**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: Креатесвапчаинфоркоревиндов**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)или [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) для описания использования поверхности и параметров доступа ЦП для заднего буфера цепочки буферов. Вы не можете использовать **\_ \_ Общие сведения об использовании DXGI**, отменять их использование, а **\_ \_ \_ на \_** **DXGI — \_ \_ \_ только чтение** значений в качестве входных данных для создания цепочки буфера обмена. Однако DXGI может устанавливать **\_ \_ отмену использования DXGI \_ в \_ настоящее** время **и \_ использование \_ DXGI \_ только для чтения** для некоторых задних буферов цепочки буфера обмена от имени приложения. Чтобы получить сведения об использовании этих задних буферов, можно вызвать метод [**идксгиресаурце:: Usage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) . Цепь подкачки поддерживает значение " **\_ доступ ЦП \_ DXGI \_ None** " в **поле " \_ \_ доступ к \_ ЦП** DXGI" в разделе " **\_ Использование DXGI**".

Эти параметры флагов также используются методом [**идксгидевице:: креатесурфаце**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




