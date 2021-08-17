---
description: Windows отправляет всем окнам верхнего уровня набор сообщений WM девицечанже по умолчанию \_ при добавлении новых устройств или носителей (например, компакт-диск или DVD), а также при удалении существующих устройств или носителей.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Обнаружение вставки или удаления носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3f6d579ed654ae2d2f77d00f70b88dc1441d03bbce59c0f8cb39ca6800c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318354"
---
# <a name="detecting-media-insertion-or-removal"></a>Обнаружение вставки или удаления носителя

Windows отправляет всем окнам верхнего уровня набор сообщений [**WM \_ девицечанже**](wm-devicechange.md) по умолчанию при добавлении новых устройств или носителей (например, компакт-диск или DVD), а также при удалении существующих устройств или носителей. Для получения этих сообщений по умолчанию регистрация не требуется. Дополнительные сведения о том, какие сообщения отправляются по умолчанию, см. в разделе "Примечания" в [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) . Сообщения в приведенном ниже примере кода являются сообщениями по умолчанию.

> [!Note]  
> Windows отправляет сообщения [**WM \_ девицечанже**](wm-devicechange.md) только для событий носителя CD или DVD в окна верхнего уровня, принадлежащие приложениям, выполняемым в активном сеансе консоли. Окна верхнего уровня, принадлежащие приложениям, выполняемым в сеансе удаленного рабочего стола, не получают [**сообщения \_ девицечанже WM**](wm-devicechange.md) для событий носителя CD или DVD.

 

Каждое [**сообщение \_ девицечанже WM**](wm-devicechange.md) имеет связанное событие, описывающее изменение, и структуру, которая предоставляет подробные сведения об изменении. Структура состоит из заголовков, не зависящих от событий, а также для [**\_ \_ HDR-вещания dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), за которыми следуют элементы, зависимые от событий. Зависимые от события члены описывают устройство, к которому применяется событие. Чтобы использовать эту структуру, приложения должны сначала определить тип события и тип устройства. Затем они могут использовать правильную структуру для выполнения соответствующих действий.

Когда пользователь вставляет новый компакт-диск или DVD-диск в дисковод, приложения получают сообщение [**WM \_ девицечанже**](wm-devicechange.md) с событием [ \_ девицеарривал ДБТ](dbt-devicearrival.md) . Приложение должно проверить событие, чтобы убедиться, что тип, поступающий от устройства, является томом (член **дбч \_ типа устройства** — **ДБТ \_ девтип \_ том**) и что изменение влияет на носитель (член **дбкв \_ flags** является **дбтф \_ Media**).

Когда пользователь удаляет компакт-диск или DVD-диск из накопителя, приложения получают сообщение [**WM \_ девицечанже**](wm-devicechange.md) с событием [ \_ девицеремовекомплете ДБТ](dbt-deviceremovecomplete.md) . Опять же, приложение должно проверить событие, чтобы убедиться, что удаляемое устройство является томом и что изменение влияет на носитель.

В следующем коде показано, как проверить вставку или удаление компакт-диска или DVD.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[События устройства](device-events.md)
</dt> </dl>

 

 



