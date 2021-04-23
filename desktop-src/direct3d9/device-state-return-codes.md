---
description: Список некоторых возможных кодов возврата для методов и функций.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262361"
---
# <a name="s_present"></a><span data-ttu-id="752c7-103">\_есть</span><span class="sxs-lookup"><span data-stu-id="752c7-103">S\_PRESENT</span></span>

<span data-ttu-id="752c7-104">Список некоторых возможных кодов возврата для методов и функций.</span><span class="sxs-lookup"><span data-stu-id="752c7-104">A list of some of the possible return codes for methods and functions.</span></span>



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752c7-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="752c7-105">\#define</span></span>                  | <span data-ttu-id="752c7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="752c7-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="752c7-107">\_ОК</span><span class="sxs-lookup"><span data-stu-id="752c7-107">S\_OK</span></span>                     | <span data-ttu-id="752c7-108">Устройство работает нормально и может использоваться для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="752c7-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="752c7-109">\_есть \_ перекрыто</span><span class="sxs-lookup"><span data-stu-id="752c7-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="752c7-110">Область презентации — перекрыто.</span><span class="sxs-lookup"><span data-stu-id="752c7-110">The presentation area is occluded.</span></span> <span data-ttu-id="752c7-111">Перекрытия означает, что окно презентации является сведенным, или другое устройство перешло на полноэкранный режим на том же мониторе, что и окно презентации, и окно презентации полностью находится на этом мониторе.</span><span class="sxs-lookup"><span data-stu-id="752c7-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="752c7-112">Перекрытия не будет выполняться, если область клиента охватывается другим окном.</span><span class="sxs-lookup"><span data-stu-id="752c7-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="752c7-113">Приложения перекрыто могут продолжить отрисовку, и все вызовы будут выполнены, но окно презентации перекрыто не будет обновлено.</span><span class="sxs-lookup"><span data-stu-id="752c7-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="752c7-114">Желательно, чтобы приложение не применяло отрисовку в окне презентации с помощью устройства и продолжало вызывать [**чеккдевицестате**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) до тех пор, пока не \_ \_ \_ изменится режим отображения ОК или s \_ .</span><span class="sxs-lookup"><span data-stu-id="752c7-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="752c7-115">\_ \_ изменен режим представления \_</span><span class="sxs-lookup"><span data-stu-id="752c7-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="752c7-116">Режим экрана рабочего стола изменен.</span><span class="sxs-lookup"><span data-stu-id="752c7-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="752c7-117">Приложение может продолжить подготовку к просмотру, но может быть выполнено преобразование или растяжение цвета.</span><span class="sxs-lookup"><span data-stu-id="752c7-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="752c7-118">Выберите формат обратного буфера, аналогичный текущему режиму экрана, и вызовите сброс для повторного создания цепочек подкачки.</span><span class="sxs-lookup"><span data-stu-id="752c7-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="752c7-119">Устройство останется в этом состоянии после вызова сброса.</span><span class="sxs-lookup"><span data-stu-id="752c7-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="752c7-120">Другие коды ошибок содержатся в [D3DERR](d3derr.md).</span><span class="sxs-lookup"><span data-stu-id="752c7-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="752c7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="752c7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="752c7-122">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="752c7-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




