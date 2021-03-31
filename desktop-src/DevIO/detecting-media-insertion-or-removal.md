---
description: Windows отправляет все окна верхнего уровня как набор сообщений WM девицечанже по умолчанию \_ при добавлении новых устройств или носителей (таких как компакт-диск или диск DVD), а также при удалении существующих устройств или носителей.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Обнаружение вставки или удаления носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157015"
---
# <a name="detecting-media-insertion-or-removal"></a><span data-ttu-id="cda6e-103">Обнаружение вставки или удаления носителя</span><span class="sxs-lookup"><span data-stu-id="cda6e-103">Detecting Media Insertion or Removal</span></span>

<span data-ttu-id="cda6e-104">Windows отправляет все окна верхнего уровня как набор сообщений [**WM \_ девицечанже**](wm-devicechange.md) по умолчанию при добавлении новых устройств или носителей (таких как компакт-диск или диск DVD), а также при удалении существующих устройств или носителей.</span><span class="sxs-lookup"><span data-stu-id="cda6e-104">Windows sends all top-level windows a set of default [**WM\_DEVICECHANGE**](wm-devicechange.md) messages when new devices or media (such as a CD or DVD) are added and become available, and when existing devices or media are removed.</span></span> <span data-ttu-id="cda6e-105">Для получения этих сообщений по умолчанию регистрация не требуется.</span><span class="sxs-lookup"><span data-stu-id="cda6e-105">You do not need to register to receive these default messages.</span></span> <span data-ttu-id="cda6e-106">Дополнительные сведения о том, какие сообщения отправляются по умолчанию, см. в разделе "Примечания" в [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="cda6e-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details on which messages are sent by default.</span></span> <span data-ttu-id="cda6e-107">Сообщения в приведенном ниже примере кода являются сообщениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cda6e-107">The messages in the code example below are among the default messages.</span></span>

> [!Note]  
> <span data-ttu-id="cda6e-108">Windows отправляет сообщения [**WM \_ девицечанже**](wm-devicechange.md) только для событий компакт-дисков или DVD в окна верхнего уровня, принадлежащие приложениям, выполняемым в активном сеансе консоли.</span><span class="sxs-lookup"><span data-stu-id="cda6e-108">Windows only sends [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events to top-level windows that are owned by applications that run in the active console session.</span></span> <span data-ttu-id="cda6e-109">Окна верхнего уровня, принадлежащие приложениям, выполняемым в сеансе удаленного рабочего стола, не получают [**сообщения \_ девицечанже WM**](wm-devicechange.md) для событий носителя CD или DVD.</span><span class="sxs-lookup"><span data-stu-id="cda6e-109">Top-level windows that are owned by applications that run in a remote desktop session do not receive [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events.</span></span>

 

<span data-ttu-id="cda6e-110">Каждое [**сообщение \_ девицечанже WM**](wm-devicechange.md) имеет связанное событие, описывающее изменение, и структуру, которая предоставляет подробные сведения об изменении.</span><span class="sxs-lookup"><span data-stu-id="cda6e-110">Each [**WM\_DEVICECHANGE**](wm-devicechange.md) message has an associated event that describes the change, and a structure that provides detailed information about the change.</span></span> <span data-ttu-id="cda6e-111">Структура состоит из заголовков, не зависящих от событий, а также для [**\_ \_ HDR-вещания dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), за которыми следуют элементы, зависимые от событий.</span><span class="sxs-lookup"><span data-stu-id="cda6e-111">The structure consists of an event-independent header, [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), followed by event-dependent members.</span></span> <span data-ttu-id="cda6e-112">Зависимые от события члены описывают устройство, к которому применяется событие.</span><span class="sxs-lookup"><span data-stu-id="cda6e-112">The event-dependent members describe the device to which the event applies.</span></span> <span data-ttu-id="cda6e-113">Чтобы использовать эту структуру, приложения должны сначала определить тип события и тип устройства.</span><span class="sxs-lookup"><span data-stu-id="cda6e-113">To use this structure, applications must first determine the event type and the device type.</span></span> <span data-ttu-id="cda6e-114">Затем они могут использовать правильную структуру для выполнения соответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="cda6e-114">Then, they can use the correct structure to take appropriate action.</span></span>

<span data-ttu-id="cda6e-115">Когда пользователь вставляет новый компакт-диск или DVD-диск в дисковод, приложения получают сообщение [**WM \_ девицечанже**](wm-devicechange.md) с событием [ \_ девицеарривал ДБТ](dbt-devicearrival.md) .</span><span class="sxs-lookup"><span data-stu-id="cda6e-115">When the user inserts a new CD or DVD into a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEARRIVAL](dbt-devicearrival.md) event.</span></span> <span data-ttu-id="cda6e-116">Приложение должно проверить событие, чтобы убедиться, что тип, поступающий от устройства, является томом (член **дбч \_ типа устройства** — **ДБТ \_ девтип \_ том**) и что изменение влияет на носитель (член **дбкв \_ flags** является **дбтф \_ Media**).</span><span class="sxs-lookup"><span data-stu-id="cda6e-116">The application must check the event to ensure that the type of device arriving is a volume (the **dbch\_devicetype** member is **DBT\_DEVTYP\_VOLUME**) and that the change affects the media (the **dbcv\_flags** member is **DBTF\_MEDIA**).</span></span>

<span data-ttu-id="cda6e-117">Когда пользователь удаляет компакт-диск или DVD-диск из накопителя, приложения получают сообщение [**WM \_ девицечанже**](wm-devicechange.md) с событием [ \_ девицеремовекомплете ДБТ](dbt-deviceremovecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="cda6e-117">When the user removes a CD or DVD from a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) event.</span></span> <span data-ttu-id="cda6e-118">Опять же, приложение должно проверить событие, чтобы убедиться, что удаляемое устройство является томом и что изменение влияет на носитель.</span><span class="sxs-lookup"><span data-stu-id="cda6e-118">Again, the application must check the event to ensure that the device being removed is a volume and that the change affects the media.</span></span>

<span data-ttu-id="cda6e-119">В следующем коде показано, как проверить вставку или удаление компакт-диска или DVD.</span><span class="sxs-lookup"><span data-stu-id="cda6e-119">The following code demonstrates how to check for insertion or removal of a CD or DVD.</span></span>


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
#pragma comment(lib, "user32.lib" )

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam );
char FirstDriveFromMask( ULONG unitmask );  //prototype

/*------------------------------------------------------------------
   Main_OnDeviceChange( hwnd, wParam, lParam )

   Description
      Handles WM_DEVICECHANGE messages sent to the application's
      top-level window.
--------------------------------------------------------------------*/

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam )
 {
  PDEV_BROADCAST_HDR lpdb = (PDEV_BROADCAST_HDR)lParam;
  TCHAR szMsg[80];

  switch(wParam )
   {
    case DBT_DEVICEARRIVAL:
      // Check whether a CD or DVD was inserted into a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media has arrived.\n"), 
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE"), MB_OK );
         }
       }
      break;

    case DBT_DEVICEREMOVECOMPLETE:
      // Check whether a CD or DVD was removed from a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media was removed.\n" ),
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE" ), MB_OK );
         }
       }
      break;

    default:
      /*
        Process other WM_DEVICECHANGE notifications for other 
        devices or reasons.
      */ 
      ;
   }
}

/*------------------------------------------------------------------
   FirstDriveFromMask( unitmask )

   Description
     Finds the first valid drive letter from a mask of drive letters.
     The mask must be in the format bit 0 = A, bit 1 = B, bit 2 = C, 
     and so on. A valid drive letter is defined when the 
     corresponding bit is set to 1.

   Returns the first drive letter that was found.
--------------------------------------------------------------------*/

char FirstDriveFromMask( ULONG unitmask )
 {
  char i;

  for (i = 0; i < 26; ++i)
   {
    if (unitmask & 0x1)
      break;
    unitmask = unitmask >> 1;
   }

  return( i + 'A' );
}
```



## <a name="related-topics"></a><span data-ttu-id="cda6e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cda6e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cda6e-121">События устройства</span><span class="sxs-lookup"><span data-stu-id="cda6e-121">Device Events</span></span>](device-events.md)
</dt> </dl>

 

 



