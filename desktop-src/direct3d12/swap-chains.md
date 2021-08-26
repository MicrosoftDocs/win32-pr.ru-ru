---
title: Цепочки буферов
description: Цепи переключения управляют поворотом заднего буфера, формируя основание графической анимации.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e98fc2baf63d7d80fefc190f2d01da33ea24d420e647b4f0c57df7ec4c501f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850654"
---
# <a name="swap-chains"></a>Цепочки буферов

Цепи переключения управляют поворотом заднего буфера, формируя основание графической анимации.

## <a name="overview"></a>Обзор

Модель программирования для цепочек подкачки в Direct3D 12 не совпадает с моделью в более ранних версиях D3D. Удобство программирования, например, для поддержки автоматического вращения ресурсов, которое присутствовало в D3D10 и D3D11, теперь не поддерживается. Автоматические приложения с включенным поворотом ресурсов отображают один и тот же объект API, в то время как фактически отображаемая поверхность изменяет каждый кадр. Поведение цепочек подкачки изменяется с помощью Direct3D 12, чтобы другие функции Direct3D 12 могли снизить нагрузку ЦП. Автоматический цветовой ключ и множественная выборка не поддерживаются, хотя, по-прежнему, выполняется растяжение и вращение.

### <a name="buffer-lifetime"></a>Время существования буфера

Приложения могут хранить предварительно созданные дескрипторы, ссылающиеся на обратные буферы. это можно сделать, убедившись, что набор буферов, принадлежащих цепи подкачки, никогда не изменится в течение времени существования цепочки буфера обмена. Набор буферов, возвращаемых функцией [**идксгисвапчаин::-buffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) , не изменяется, пока не вызваны определенные API:

-   [**Идксгисвапчаин:: Ресизетаржет**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**Идксгисвапчаин:: Ресизебуфферс**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

Порядок буферов, возвращаемых методом [**buffer, никогда не**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) изменяется.

[**IDXGISwapChain3:: жеткуррентбаккбуффериндекс**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) возвращает индекс текущего заднего буфера приложения.

### <a name="swap-effects"></a>Переключить эффекты

Единственными поддерживаемыми эффектами переключения являются [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) и [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), для которых количество буферов должно быть больше единицы.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Переход между оконным и полноэкранным режимами

Direct3D 12 не поддерживает полноэкранный монопольный режим (FSE). Вместо этого, когда игра является единственным видимым приложением на экране, в операционной системе используется стратегия, называемая полноэкранными оптимизациями (FSO), для достижения аналогичного результата работы программы FSE без снижения производительности. Дополнительные сведения о FSO см. в разделе [пояснения к полноэкранным оптимизациям](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).

Direct3D 12 поддерживает ограничение, которое приложения должны вызывать [**ресизебуфферс**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) после перехода между оконным и полноэкранным режимами (ЦЕПОЧКи D3D11 перелистывания моделей имеют те же ограничения).

Переходы [**идксгисвапчаин:: сетфуллскринстате**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) не изменяют набор видимых для приложения буферов в цепочке буфера обмена. Только [**ресизебуфферс**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) и [**ресизетаржет**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) вызывают создание или удаление видимых для приложения буферов. Однако в Direct3D 12 [**идксгисвапчаин:: сетфуллскринстате**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) не переходит в полноэкранный режим монопольного доступа и просто изменяет разрешения и скорости обновления, чтобы разрешить полноэкранное ускорение. Эти изменения могут выполняться приложением без использования этого метода.

Когда или [**идксгисвапчаин::P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) повторная отправка или [**IDXGISwapChain1:P:**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) вызывается повторная отправка, возвращенный буфер должен находиться в [**состоянии \_ ресурса \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) . Present завершается с **ошибкой \_ \_ Недопустимый \_ вызов функции DXGI** , если это не так.

Цепочки полноэкранного переключения по-прежнему имеют ограничение, которое [**сетфуллскринстате**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(false, null) должно быть вызвано до окончательного выпуска цепочки буферов. **Сетфуллскринстате**(false) в цепочках подкачки, выполняющихся на устройствах Direct3D 12, проходит.

Операции, выполняемые в трехмерной очереди, задаются при создании имеющуюся цепочку буферов, а приложения могут параллельно представлять несколько цепочек переключения, а также записывать и выполнять списки команд.

Когда окончательная часть графической работы (например, поэтапная обработка кадров) выполняется в очереди вычислений или не участвует в очереди графики устройства, создание второй объемной очереди для отображения в может оказаться полезным и предотвратить задержку показа в начале следующего кадра. 

### <a name="example"></a>Пример

Следующий пример кода будет представлен в основном цикле визуализации:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Создание цепочек подкачки

При использовании вызовов [**креатесвапчаинфорхвнд**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**креатесвапчаинфоркоревиндов**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)или [**креатесвапчаинфоркомпоситион**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) Обратите внимание, что параметр *pDevice* на самом деле требует наличия указателя на прямую командную очередь в Direct3D 12, а не на устройстве.

### <a name="presenting-on-windows-7"></a>презентация на Windows 7

при использовании direct3d 12 на Windows 7 необходимые типы DXGI для Direct3D 12 отсутствуют, поэтому необходимо использовать **ID3D12CommandQueueDownLevel** , предоставленный D3D12On7 (запрошенный из прямой очереди команд).

вы предоставляете список открытых команд для метода Windows 7 present, который затем будет использоваться, закрыт и автоматически отправлен на устройство. Необходимо указать задний буфер, который должен быть создан приложением, должен быть зафиксированным ресурсом, должен быть единственным образцом и должен иметь один из следующих форматов.

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>Связанные темы

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [Видеоучебники по расширенному обучению DirectX: нерегулируемая частота кадров](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Отрисовка](rendering.md)
