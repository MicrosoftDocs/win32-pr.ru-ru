---
description: Отображение диалоговых окон записи VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Отображение диалоговых окон записи VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805387"
---
# <a name="display-vfw-capture-dialog-boxes"></a><span data-ttu-id="af10e-103">Отображение диалоговых окон записи VFW</span><span class="sxs-lookup"><span data-stu-id="af10e-103">Display VFW Capture Dialog Boxes</span></span>

<span data-ttu-id="af10e-104">Устройство записи, которое по-прежнему использует драйвер Video для Windows (VFW), может поддерживать любое из следующих трех диалоговых окон, которые используются для настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="af10e-104">A capture device that still uses a Video for Windows (VFW) driver can support any of the following three dialog boxes, which are used to configure the device.</span></span>



| <span data-ttu-id="af10e-105">.</span><span class="sxs-lookup"><span data-stu-id="af10e-105">Dialog box</span></span>    | <span data-ttu-id="af10e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="af10e-106">Description</span></span>                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af10e-107">Источник видео</span><span class="sxs-lookup"><span data-stu-id="af10e-107">Video Source</span></span>  | <span data-ttu-id="af10e-108">Используется для выбора входных данных видео и для настройки параметров устройства, таких как яркость или контрастность изображения.</span><span class="sxs-lookup"><span data-stu-id="af10e-108">Used to select the video input and to adjust device settings, such as picture brightness or contrast.</span></span> |
| <span data-ttu-id="af10e-109">Формат видео</span><span class="sxs-lookup"><span data-stu-id="af10e-109">Video Format</span></span>  | <span data-ttu-id="af10e-110">Используется для выбора размеров изображения и битовой глубины.</span><span class="sxs-lookup"><span data-stu-id="af10e-110">Used to select the image dimensions and bit depth.</span></span>                                                    |
| <span data-ttu-id="af10e-111">Отображение видео</span><span class="sxs-lookup"><span data-stu-id="af10e-111">Video Display</span></span> | <span data-ttu-id="af10e-112">Используется для управления внешним видом отображаемого видео.</span><span class="sxs-lookup"><span data-stu-id="af10e-112">Used to control the appearance of the rendered video.</span></span>                                                 |



 

<span data-ttu-id="af10e-113">Чтобы отобразить одно из этих диалоговых окон, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="af10e-113">To show one of these dialog boxes, do the following:</span></span>

1.  <span data-ttu-id="af10e-114">Останавливает граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="af10e-114">Stop the filter graph.</span></span>
2.  <span data-ttu-id="af10e-115">Запросите фильтр записи для интерфейса [**иамвфвкаптуредиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) .</span><span class="sxs-lookup"><span data-stu-id="af10e-115">Query the capture filter for the [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) interface.</span></span> <span data-ttu-id="af10e-116">Если **QueryInterface** проходит успешнее, это означает, что устройство записи является устройством VFW.</span><span class="sxs-lookup"><span data-stu-id="af10e-116">If **QueryInterface** succeeds, it means the capture device is a VFW device.</span></span>
3.  <span data-ttu-id="af10e-117">Вызовите метод [**иамвфвкаптуредиалогс:: хасдиалог**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) , чтобы проверить, поддерживает ли драйвер диалоговое окно, которое необходимо отобразить.</span><span class="sxs-lookup"><span data-stu-id="af10e-117">Call [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) to check if the driver supports the dialog box that you wish to display.</span></span> <span data-ttu-id="af10e-118">Перечисление [**вфвкаптуредиалогс**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) определяет флаги для каждого из диалоговых окон VFW.</span><span class="sxs-lookup"><span data-stu-id="af10e-118">The [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) enumeration defines flags for each of the VFW dialog boxes.</span></span> <span data-ttu-id="af10e-119">**Хасдиалог** возвращает значение \_ ОК, если диалоговое окно поддерживается.</span><span class="sxs-lookup"><span data-stu-id="af10e-119">**HasDialog** returns S\_OK if the dialog box is supported.</span></span> <span data-ttu-id="af10e-120">\_В противном случае возвращается значение false, поэтому следует проверить наличие значения \_ ОК напрямую, а не использовать макрос **успешно** .</span><span class="sxs-lookup"><span data-stu-id="af10e-120">It returns S\_FALSE otherwise, so check for the value S\_OK directly, rather than using the **SUCCEEDED** macro.</span></span>
4.  <span data-ttu-id="af10e-121">Если диалоговое окно поддерживается, вызовите метод [**иамвфвкаптуредиалогс:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) , чтобы отобразить диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="af10e-121">If the dialog box is supported, call [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) to display the dialog box.</span></span>
5.  <span data-ttu-id="af10e-122">Перезапустите граф.</span><span class="sxs-lookup"><span data-stu-id="af10e-122">Restart the graph.</span></span>

<span data-ttu-id="af10e-123">В следующем коде показаны эти шаги для диалогового окна источник видео.</span><span class="sxs-lookup"><span data-stu-id="af10e-123">The following code shows these steps for the Video Source dialog box:</span></span>


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a><span data-ttu-id="af10e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="af10e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af10e-125">Настройка устройства видеозаписи</span><span class="sxs-lookup"><span data-stu-id="af10e-125">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



