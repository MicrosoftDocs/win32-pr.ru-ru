---
title: Изменение свойства Scale
description: Изменение свойства Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Подключаемые модули проигрывателя Windows Media, пример свойств Echo
- подключаемые модули, свойства образца Echo
- подключаемые модули обработки цифровых сигналов, свойства образца эха
- Подключаемые модули DSP, свойства образца Echo
- Пример подключаемого модуля Echo DSP, свойство Scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691192"
---
# <a name="modifying-the-scale-property"></a><span data-ttu-id="f3fe7-108">Изменение свойства Scale</span><span class="sxs-lookup"><span data-stu-id="f3fe7-108">Modifying the Scale Property</span></span>

<span data-ttu-id="f3fe7-109">Реализация мастера по умолчанию предоставляет свойство Scale.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-109">The default wizard implementation exposes the scale property.</span></span> <span data-ttu-id="f3fe7-110">Вместо этого можно изменить существующую реализацию, чтобы предоставить свойство времени задержки.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-110">You can change the existing implementation to expose the delay time property instead.</span></span>

<span data-ttu-id="f3fe7-111">Во-первых, используйте следующий пример, чтобы изменить прототипы функций для получения \_ масштабирования и разместить \_ масштаб в Echo. h.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-111">First, use the following example to change the function prototypes for get\_scale and put\_scale in Echo.h.</span></span> <span data-ttu-id="f3fe7-112">Измените имя методов и типы данных для параметров:</span><span class="sxs-lookup"><span data-stu-id="f3fe7-112">Change the name of the methods and the data types for the parameters:</span></span>


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



<span data-ttu-id="f3fe7-113">Затем измените реализации \_ методов Get Scale и разместить \_ Scale в Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-113">Next, change the implementations of the get\_scale and put\_scale methods in Echo.cpp.</span></span> <span data-ttu-id="f3fe7-114">Убедитесь, что код соответствует следующим примерам:</span><span class="sxs-lookup"><span data-stu-id="f3fe7-114">Make the code match the following examples:</span></span>


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



<span data-ttu-id="f3fe7-115">В предыдущем примере кода изменяются имена методов и типы данных параметров.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-115">The preceding example code changes the method names and the parameter data types.</span></span> <span data-ttu-id="f3fe7-116">Имя переменной члена должно быть изменено ранее.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-116">The member variable name should have been changed previously.</span></span> <span data-ttu-id="f3fe7-117">Не забудьте изменить комментарии, которые также посвящены каждому методу.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-117">Remember to change the comments that introduce each method as well.</span></span>

<span data-ttu-id="f3fe7-118">Теперь измените определение интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-118">Now, change the interface definition.</span></span> <span data-ttu-id="f3fe7-119">Следующий код заменяет код в объявлении интерфейса Иечо в Echo. IDL:</span><span class="sxs-lookup"><span data-stu-id="f3fe7-119">The following code replaces the code in the IEcho interface declaration in Echo.idl:</span></span>


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a><span data-ttu-id="f3fe7-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f3fe7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3fe7-121">**Свойства образца Echo**</span><span class="sxs-lookup"><span data-stu-id="f3fe7-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




