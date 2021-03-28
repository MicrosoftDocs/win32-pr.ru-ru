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
# <a name="how-to-get-adapter-display-modes"></a>Как получить режимы отображения адаптера

В этом разделе показано, как использовать графическую инфраструктуру Microsoft DirectX (DXGI) для получения допустимых режимов отображения, связанных с адаптером. DirectX 10 и 11 могут использовать DXGI для получения допустимых режимов экрана. Знание допустимых режимов отображения гарантирует, что приложение сможет правильно выбрать допустимый полноэкранный режим.

**Получение режима вывода адаптера**

1.  Создайте объект [**идксгифактори**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) и используйте его для перечисления доступных адаптеров. Дополнительные сведения см. [в разделе руководство. Перечисление адаптеров](overviews-direct3d-11-devices-enum.md).
2.  Вызовите метод Идксгиадаптер:: Енумаутпутс, чтобы перечислить выходные данные для каждого адаптера.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Вызовите метод Идксгиаутпут:: Жетдисплаймоделист, чтобы извлечь [**массив \_ \_ DESC в режиме DXGI**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) и количество элементов в массиве. Каждая **Структура \_ \_ DESC в режиме DXGI** представляет собой допустимый режим вывода для выходных данных.
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

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устройства](overviews-direct3d-11-devices.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 