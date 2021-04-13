---
title: Прототипы
description: Прототипы
ms.assetid: 2b31c01b-d52b-4df5-9cb0-a35286febd3a
keywords:
- Платформа текстовых служб (TSF), прототипы
- TSF (платформа текстовых служб), прототипы
- Справочник по TSF, прототипы
- Справочник по TSF, прототипам
- текстовые службы, прототипы
- Приложения с поддержкой TSF, прототипы
- прототипы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6212461b45d65b73caa77cf21b7591a77ef2a199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413053"
---
# <a name="prototypes"></a><span data-ttu-id="a84f9-110">Прототипы</span><span class="sxs-lookup"><span data-stu-id="a84f9-110">Prototypes</span></span>

<span data-ttu-id="a84f9-111">[Итфконтекстрендерингмаркуп](/windows/desktop/TSF/itfcontextrenderingmarkup), [иенумтфрендерингмаркуп](/windows/desktop/TSF/ienumtfrenderingmarkup)и [tf \_ рендерингмаркуп](/windows/desktop/TSF/tf-renderingmarkup) , описанные в этой ссылке, не определены в файлах IDL или в заголовочном файле.</span><span class="sxs-lookup"><span data-stu-id="a84f9-111">[ITfContextRenderingMarkup](/windows/desktop/TSF/itfcontextrenderingmarkup), [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup), and [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) described in this reference are not defined in IDL or header files.</span></span> <span data-ttu-id="a84f9-112">Для того чтобы получить файл заголовка, необходимо, чтобы компилятор MIDL выполнял следующие прототипы.</span><span class="sxs-lookup"><span data-stu-id="a84f9-112">The following prototypes are needed to be complied by MIDL compiler to get the header file..</span></span>


```C++
typedef struct
{
    ITfRange *pRange;
    TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;

// 
// IEnumTfRenderingMarkup 
// 
[
  object,
  uuid(8c03d21b-95a7-4ba0-ae1b-7fce12a72930),
  pointer_default(unique)
]
interface IEnumTfRenderingMarkup : IUnknown
{
    HRESULT Clone([out] IEnumTfRenderingMarkup **ppClone);

    HRESULT Next([in] ULONG ulCount,
                 [out, size_is(ulCount), length_is(*pcFetched)] TF_RENDERINGMARKUP *rgMarkup,
                 [out] ULONG *pcFetched);

    HRESULT Reset();

    HRESULT Skip([in] ULONG ulCount);
};

// 
// ITfContextRenderingMarkup 
// 
[
  object,
  uuid(a305b1c0-c776-4523-bda0-7c5a2e0fef10),
  pointer_default(unique)
]
interface ITfContextRenderingMarkup : IUnknown
{
    const DWORD TF_GRM_INCLUDE_PROPERTY = 0x1;

    HRESULT GetRenderingMarkup([in] TfEditCookie ec,
                               [in] DWORD dwFlags,
                               [in] ITfRange *pRangeCover,
                               [out] IEnumTfRenderingMarkup **ppEnum);
                                                           
    HRESULT FindNextRenderingMarkup([in] TfEditCookie ec,
                                    [in] DWORD dwFlags,
                                    [in] ITfRange *pRangeQuery,
                                    [in] TfAnchor tfAnchorQuery,
                                    [out] ITfRange **ppRangeFound,
                                    [out] TF_RENDERINGMARKUP *ptfRenderingMarkup);
};
```



 

 