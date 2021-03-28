---
title: Получение режимов отображения адаптера
description: В этом разделе показано, как использовать графическую инфраструктуру Microsoft DirectX (DXGI) для получения допустимых режимов отображения, связанных с адаптером.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c2602fcd4e1baa4476bb89273eda676f444e38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337572"
---
# <a name="how-to-get-adapter-display-modes"></a><span data-ttu-id="5e6cd-103">Как получить режимы отображения адаптера</span><span class="sxs-lookup"><span data-stu-id="5e6cd-103">How To: Get Adapter Display Modes</span></span>

<span data-ttu-id="5e6cd-104">В этом разделе показано, как использовать графическую инфраструктуру Microsoft DirectX (DXGI) для получения допустимых режимов отображения, связанных с адаптером.</span><span class="sxs-lookup"><span data-stu-id="5e6cd-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to get the valid display modes associated with an adapter.</span></span> <span data-ttu-id="5e6cd-105">DirectX 10 и 11 могут использовать DXGI для получения допустимых режимов экрана.</span><span class="sxs-lookup"><span data-stu-id="5e6cd-105">DirectX 10 and 11 can use DXGI to get the valid display modes.</span></span> <span data-ttu-id="5e6cd-106">Знание допустимых режимов отображения гарантирует, что приложение сможет правильно выбрать допустимый полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="5e6cd-106">Knowing the valid display modes ensures that your application can properly choose a valid full-screen mode.</span></span>

<span data-ttu-id="5e6cd-107">**Получение режима вывода адаптера**</span><span class="sxs-lookup"><span data-stu-id="5e6cd-107">**To get adapter display modes**</span></span>

1.  <span data-ttu-id="5e6cd-108">Создайте объект [**идксгифактори**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) и используйте его для перечисления доступных адаптеров.</span><span class="sxs-lookup"><span data-stu-id="5e6cd-108">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object and use it to enumerate the available adapters.</span></span> <span data-ttu-id="5e6cd-109">Дополнительные сведения см. [в разделе руководство. Перечисление адаптеров](overviews-direct3d-11-devices-enum.md).</span><span class="sxs-lookup"><span data-stu-id="5e6cd-109">For more information, see [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).</span></span>
2.  <span data-ttu-id="5e6cd-110">Вызовите метод Идксгиадаптер:: Енумаутпутс, чтобы перечислить выходные данные для каждого адаптера.</span><span class="sxs-lookup"><span data-stu-id="5e6cd-110">Call IDXGIAdapter::EnumOutputs to enumerate the outputs for each adapter.</span></span>
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  <span data-ttu-id="5e6cd-111">Вызовите метод Идксгиаутпут:: Жетдисплаймоделист, чтобы извлечь [**массив \_ \_ DESC в режиме DXGI**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) и количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="5e6cd-111">Call IDXGIOutput::GetDisplayModeList to retrieve an array of [**DXGI\_MODE\_DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) structures and the number of elements in the array.</span></span> <span data-ttu-id="5e6cd-112">Каждая **Структура \_ \_ DESC в режиме DXGI** представляет собой допустимый режим вывода для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5e6cd-112">Each **DXGI\_MODE\_DESC** structure represents a valid display mode for the output.</span></span>
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5e6cd-113">См. также</span><span class="sxs-lookup"><span data-stu-id="5e6cd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e6cd-114">Устройства</span><span class="sxs-lookup"><span data-stu-id="5e6cd-114">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="5e6cd-115">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5e6cd-115">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 