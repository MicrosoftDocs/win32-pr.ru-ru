---
title: Работа с портативными устройствами
description: Работа с портативными устройствами
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Проигрыватель Windows Media, переносные устройства
- Объектная модель проигрывателя Windows Media, переносные устройства
- Объектная модель, портативные устройства
- Элемент управления ActiveX проигрывателя Windows Media, переносные устройства
- Элемент управления ActiveX, переносные устройства
- Мобильный элемент управления ActiveX проигрывателя Windows Media, портативные устройства
- Проигрыватель Windows Media Mobile, переносные устройства
- портативные устройства, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332379"
---
# <a name="working-with-portable-devices"></a><span data-ttu-id="5ec92-111">Работа с портативными устройствами</span><span class="sxs-lookup"><span data-stu-id="5ec92-111">Working with Portable Devices</span></span>

<span data-ttu-id="5ec92-112">В этом разделе описывается использование удаленного элемента управления ActiveX проигрывателя Windows Media для работы с портативными устройствами.</span><span class="sxs-lookup"><span data-stu-id="5ec92-112">This section describes how to use a remoted Windows Media Player ActiveX control to work with portable devices.</span></span>

<span data-ttu-id="5ec92-113">В примерах кода в этом разделе используются классы библиотеки активных шаблонов (ATL), такие как **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="5ec92-113">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="5ec92-114">Включаемые заголовки</span><span class="sxs-lookup"><span data-stu-id="5ec92-114">Included Headers</span></span>

<span data-ttu-id="5ec92-115">Чтобы использовать код в этом разделе, включите следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="5ec92-115">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a><span data-ttu-id="5ec92-116">Ивмпплайер, указатель</span><span class="sxs-lookup"><span data-stu-id="5ec92-116">IWMPPlayer Pointer</span></span>

<span data-ttu-id="5ec92-117">Указатель **ивмпплайер** хранится в переменной-члене.</span><span class="sxs-lookup"><span data-stu-id="5ec92-117">The **IWMPPlayer** pointer is stored in a member variable.</span></span>


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a><span data-ttu-id="5ec92-118">Устройства хранятся в массиве</span><span class="sxs-lookup"><span data-stu-id="5ec92-118">Devices are Stored in an Array</span></span>

<span data-ttu-id="5ec92-119">Пример кода обращается к следующей переменной члена для объявления в заголовке проекта:</span><span class="sxs-lookup"><span data-stu-id="5ec92-119">The example code accesses the following member variable, to be declared in the project header:</span></span>


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



<span data-ttu-id="5ec92-120">Число устройств хранится в переменной-члене.</span><span class="sxs-lookup"><span data-stu-id="5ec92-120">The device count is stored in a member variable.</span></span>


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a><span data-ttu-id="5ec92-121">Получение указателя устройства</span><span class="sxs-lookup"><span data-stu-id="5ec92-121">Retrieving a Device Pointer</span></span>

<span data-ttu-id="5ec92-122">Указатель на конкретное устройство извлекается через его индекс массива с помощью кода, аналогичного следующему:</span><span class="sxs-lookup"><span data-stu-id="5ec92-122">A pointer to a particular device is retrieved through its array index by using code similar to the following:</span></span>


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



<span data-ttu-id="5ec92-123">Обратите внимание, что индекс, приведенный в предыдущих примерах, не является индексом партнерства для устройства.</span><span class="sxs-lookup"><span data-stu-id="5ec92-123">Note that the index shown in the preceding examples is not the partnership index for the device.</span></span> <span data-ttu-id="5ec92-124">Это индекс устройства в настраиваемом массиве устройств.</span><span class="sxs-lookup"><span data-stu-id="5ec92-124">It is the index to the device in the custom array of devices.</span></span>

## <a name="cleaning-up"></a><span data-ttu-id="5ec92-125">Очистка</span><span class="sxs-lookup"><span data-stu-id="5ec92-125">Cleaning Up</span></span>

<span data-ttu-id="5ec92-126">В примерах используется следующая функция для освобождения памяти в массиве устройств и для освобождения указателей интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5ec92-126">The examples use the following function to free the memory in the device array and to release the interface pointers:</span></span>


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a><span data-ttu-id="5ec92-127">Устройства отображаются в окне списка</span><span class="sxs-lookup"><span data-stu-id="5ec92-127">Devices are Displayed in a List Box</span></span>

<span data-ttu-id="5ec92-128">Функция Жетселектеддевицеиндекс возвращает индекс устройства, выбранного пользователем в списке, с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="5ec92-128">The GetSelectedDeviceIndex function returns the index of the device the user selected in a list box by using the following code:</span></span>


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a><span data-ttu-id="5ec92-129">Состояние пользовательского интерфейса управляется одной функцией</span><span class="sxs-lookup"><span data-stu-id="5ec92-129">User Interface State is Managed by a Single Function</span></span>

<span data-ttu-id="5ec92-130">Функция Сетуистате управляет пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="5ec92-130">The SetUIState function manages the user interface.</span></span>


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



<span data-ttu-id="5ec92-131">Сведения этой функции не связаны с обсуждениями в этом разделе, но имейте в виду, что эта функция выполняет такие задачи, как включение или отключение элементов управления и изменение отображаемого текста в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="5ec92-131">The details of this function are not relevant to the discussions in this section, but be aware that this function performs tasks like enabling or disabling controls and changing display text in the user interface.</span></span>

<span data-ttu-id="5ec92-132">Перечисление Уистате было определено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5ec92-132">The UIState enumeration was defined as follows:</span></span>


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



<span data-ttu-id="5ec92-133">Параметр *бконнектед* указывает, следует ли настраивать пользовательский интерфейс для подключенного устройства (значение true означает, что устройство подключено).</span><span class="sxs-lookup"><span data-stu-id="5ec92-133">The *bConnected* parameter specifies whether to configure the user interface for a connected device (TRUE means the device is connected).</span></span> <span data-ttu-id="5ec92-134">Параметры *NewState* и *бконнектед* сообщают сведения, необходимые для выполнения работы функции.</span><span class="sxs-lookup"><span data-stu-id="5ec92-134">The *NewState* and *bConnected* parameters convey the information needed for the function to do its work.</span></span>

<span data-ttu-id="5ec92-135">В следующих разделах приводится объяснение кода примера.</span><span class="sxs-lookup"><span data-stu-id="5ec92-135">The following sections provide explanations of the example code:</span></span>

-   [<span data-ttu-id="5ec92-136">Перечисление устройств</span><span class="sxs-lookup"><span data-stu-id="5ec92-136">Enumerating Devices</span></span>](enumerating-devices.md)
-   [<span data-ttu-id="5ec92-137">Получение атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="5ec92-137">Retrieving Device Attributes</span></span>](retrieving-device-attributes.md)
-   [<span data-ttu-id="5ec92-138">Отображение хода выполнения синхронизации</span><span class="sxs-lookup"><span data-stu-id="5ec92-138">Showing Synchronization Progress</span></span>](showing-synchronization-progress.md)
-   [<span data-ttu-id="5ec92-139">Управление списками воспроизведения синхронизации</span><span class="sxs-lookup"><span data-stu-id="5ec92-139">Managing Synchronization Playlists</span></span>](managing-synchronization-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="5ec92-140">См. также</span><span class="sxs-lookup"><span data-stu-id="5ec92-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec92-141">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="5ec92-141">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




