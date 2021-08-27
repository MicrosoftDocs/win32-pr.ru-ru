---
title: Как получить уровень функций устройства
description: В этом разделе показано, как получить максимальный уровень функций, поддерживаемый устройством.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac21d00aeef8ae6c82ffd9f55a40415b6af1d0a780cc6878d8c30bf453457eb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119604"
---
# <a name="how-to-get-the-device-feature-level"></a>Как получить уровень функций устройства

В этом разделе показано, как получить максимальный [уровень функций](overviews-direct3d-11-devices-downlevel-intro.md) , поддерживаемый [устройством](overviews-direct3d-11-devices-intro.md). Устройства Direct3D 11 поддерживают фиксированный набор уровней функций, определенных в перечислении [**\_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Когда вы узнаете о высшем [уровне функций](overviews-direct3d-11-devices-downlevel-intro.md) , поддерживаемом устройством, вы можете использовать пути кода, подходящие для этого устройства.

**Получение уровня функций устройства**

1.  Вызовите либо функцию [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) , либо функции [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) , указав **значение NULL** для параметра *ппдевице* . Это можно сделать до создания устройства.

    \- или -

    Вызовите [**ID3D11Device:: жетфеатурелевел**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) после создания устройства.

2.  Изучите значение возвращенного [**перечисления \_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) из последнего шага, чтобы определить поддерживаемый уровень компонентов.

В следующем примере кода показано, как определить максимальный поддерживаемый уровень компонентов, вызвав функцию [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) . **D3D11CreateDevice** сохраняет максимальный поддерживаемый уровень компонентов в переменной феатурелевел. Этот код можно использовать для проверки значения перечислимого типа на [**\_ \_ уровне компонента D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) , возвращаемого **D3D11CreateDevice** . Обратите внимание, что этот код перечисляет все уровни функций явным образом (для Direct3D 11,1 и Direct3D 11,2).

> [!Note]  
> Если на компьютере установлена среда выполнения Direct3D 11,1, а *пфеатурелевелс* имеет значение **null**, эта функция не создает устройство D3D с [**\_ уровнем " \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) ". Чтобы создать устройство **с \_ \_ уровнем D3D \_ 11 \_ 1** , необходимо явным образом предоставить массив **\_ \_ уровня компонентов D3D** , включающий **\_ уровень компонента D3D \_ \_ 11 \_ 1**. Если вы предоставляете **массив \_ \_ уровня функций D3D** , содержащий **\_ уровень D3D \_ уровня \_ 11 \_ 1** на компьютере, на котором не установлена среда выполнения Direct3D 11,1, эта функция немедленно завершается с параметром E \_ INVALIDARG.

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



В разделе [справочника 10Level9](d3d11-graphics-reference-10level9.md) перечислены различия между различными методами [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) на различных уровнях функций 10Level9.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Direct3D 11 на оборудовании нижнего уровня](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




