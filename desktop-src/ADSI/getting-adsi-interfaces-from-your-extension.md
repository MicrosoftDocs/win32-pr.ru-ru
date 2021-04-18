---
title: Получение интерфейсов ADSI из расширения
description: Для расширения часто требуется получить данные из объекта каталога, к которому он привязан.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- расширения ADSI, получение интерфейсов ADSI из расширения
- ADSI ADSI, пример кода C/C++, получение интерфейсов ADSI из расширения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654373"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>Получение интерфейсов ADSI из расширения

Для расширения часто требуется получить данные из объекта каталога, к которому он привязан. Например, расширение для объекта- **компьютера** может захотеть получить значение **dnsHostName** текущего объекта из каталога. Это можно легко добиться, выполнив вызов **QueryInterface** в интерфейсе [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для агрегатора.


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



Интерфейс следует освобождать сразу после его использования. Если у расширения есть открытая ссылка на агрегатор, вы создали циклическую ссылку, и агрегатор не сможет освободить расширение. Поэтому не удается освободить агрегатор, и в результате в приложении будут обнаружены утечки памяти.

 

 