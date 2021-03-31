---
title: Функции-оболочки подключаемых модулей
description: Функции-оболочки, позволяющие вызывать открытую функцию для любого адаптера, подключенного к конвейеру, без необходимости вручную получать указатель на адаптер.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API биометрическая платформа Windows API биометрическая платформа Windows, функции-оболочки подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888947"
---
# <a name="plug-in-wrapper-functions"></a><span data-ttu-id="de521-104">Функции-оболочки подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="de521-104">Plug-in Wrapper Functions</span></span>

<span data-ttu-id="de521-105">Биометрическая платформа Windows API включает функции-оболочки, которые позволяют вызывать открытую функцию на любом адаптере, подключенном к конвейеру, без необходимости вручную получать указатель на адаптер.</span><span class="sxs-lookup"><span data-stu-id="de521-105">The Windows Biometric Framework API includes wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span> <span data-ttu-id="de521-106">Каждая оболочка проверяет входные аргументы, получает указатель адаптера и вызывает запрошенную функцию.</span><span class="sxs-lookup"><span data-stu-id="de521-106">Each wrapper checks the input arguments, retrieves an adapter pointer, and calls the requested function.</span></span> <span data-ttu-id="de521-107">Например, оболочка **вбиоенгинесесашалгорисм** имеет следующую сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="de521-107">For example, the **WbioEngineSetHashAlgorithm** wrapper has the following signature.</span></span>


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



<span data-ttu-id="de521-108">Функция проверяет, что аргумент *конвейера* не равен **null**, существует адаптер ядра и существует функция [**енгинеадаптерсесашалгорисм**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) .</span><span class="sxs-lookup"><span data-stu-id="de521-108">The function verifies that the *Pipeline* argument is not **NULL**, that an engine adapter exists, and that the [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) function exists.</span></span> <span data-ttu-id="de521-109">Все функции-оболочки определены в \_ файле заголовка адаптера винбио. h.</span><span class="sxs-lookup"><span data-stu-id="de521-109">All wrapper functions are defined in the Winbio\_adapter.h header file.</span></span> <span data-ttu-id="de521-110">В следующих разделах рассматриваются доступные оболочки.</span><span class="sxs-lookup"><span data-stu-id="de521-110">The following topics discuss the available wrappers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="de521-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="de521-111">In this section</span></span>



| <span data-ttu-id="de521-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="de521-112">Topic</span></span>                                                               | <span data-ttu-id="de521-113">Описание</span><span class="sxs-lookup"><span data-stu-id="de521-113">Description</span></span>                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de521-114">Оболочки адаптера подсистемы</span><span class="sxs-lookup"><span data-stu-id="de521-114">Engine Adapter Wrappers</span></span>](engine-adapter-wrappers.md)<br/>   | <span data-ttu-id="de521-115">Функции, которые можно использовать для вызова функций в адаптере подсистемы.</span><span class="sxs-lookup"><span data-stu-id="de521-115">Functions that you can use to call functions on your engine adapter.</span></span> <span data-ttu-id="de521-116">Эти функции определены в Винбио \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="de521-116">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="de521-117">Оболочки адаптера датчика</span><span class="sxs-lookup"><span data-stu-id="de521-117">Sensor Adapter Wrappers</span></span>](sensor-adapter-wrappers.md)<br/>   | <span data-ttu-id="de521-118">Функции, которые можно использовать для вызова функций в адаптере датчика.</span><span class="sxs-lookup"><span data-stu-id="de521-118">Functions that you can use to call functions on your sensor adapter.</span></span> <span data-ttu-id="de521-119">Эти функции определены в Винбио \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="de521-119">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="de521-120">Оболочки адаптеров хранилища</span><span class="sxs-lookup"><span data-stu-id="de521-120">Storage Adapter Wrappers</span></span>](storage-adapter-wrappers.md)<br/> | <span data-ttu-id="de521-121">Функции, которые можно использовать для вызова функций в адаптере хранилища.</span><span class="sxs-lookup"><span data-stu-id="de521-121">Functions that you can use to call functions on your storage adapter.</span></span> <span data-ttu-id="de521-122">Эти функции определены в Винбио \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="de521-122">These functions are defined in Winbio\_adapter.h.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="de521-123">См. также</span><span class="sxs-lookup"><span data-stu-id="de521-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de521-124">Справочник по подключаемым модулям</span><span class="sxs-lookup"><span data-stu-id="de521-124">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> </dl>

 

 





