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
# <a name="getting-adsi-interfaces-from-your-extension"></a><span data-ttu-id="f75de-105">Получение интерфейсов ADSI из расширения</span><span class="sxs-lookup"><span data-stu-id="f75de-105">Getting ADSI Interfaces From Your Extension</span></span>

<span data-ttu-id="f75de-106">Для расширения часто требуется получить данные из объекта каталога, к которому он привязан.</span><span class="sxs-lookup"><span data-stu-id="f75de-106">An extension often needs to get data from the directory object it binds to.</span></span> <span data-ttu-id="f75de-107">Например, расширение для объекта- **компьютера** может захотеть получить значение **dnsHostName** текущего объекта из каталога.</span><span class="sxs-lookup"><span data-stu-id="f75de-107">For example, an extension for a **computer** object may want to get the **dnsHostName** of the current object from the directory.</span></span> <span data-ttu-id="f75de-108">Это можно легко добиться, выполнив вызов **QueryInterface** в интерфейсе [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для агрегатора.</span><span class="sxs-lookup"><span data-stu-id="f75de-108">This can be easily achieved by issuing a **QueryInterface** call on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the aggregator.</span></span>


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



<span data-ttu-id="f75de-109">Интерфейс следует освобождать сразу после его использования.</span><span class="sxs-lookup"><span data-stu-id="f75de-109">You should release the interface immediately after using it.</span></span> <span data-ttu-id="f75de-110">Если у расширения есть открытая ссылка на агрегатор, вы создали циклическую ссылку, и агрегатор не сможет освободить расширение.</span><span class="sxs-lookup"><span data-stu-id="f75de-110">If the extension has an open reference to the aggregator, you have created a circular reference and the aggregator cannot release the extension.</span></span> <span data-ttu-id="f75de-111">Поэтому не удается освободить агрегатор, и в результате в приложении будут обнаружены утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="f75de-111">Therefore, the aggregator cannot be released and the result is memory leaks in your application.</span></span>

 

 