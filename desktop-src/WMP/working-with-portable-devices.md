---
title: Работа с портативными устройствами
description: Работа с портативными устройствами
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- проигрыватель Windows Media, портативные устройства
- объектная модель проигрыватель Windows Media, переносные устройства
- Объектная модель, портативные устройства
- проигрыватель Windows Media ActiveX элемент управления, портативные устройства
- ActiveX элемент управления, переносные устройства
- проигрыватель Windows Media мобильный ActiveX элемент управления, переносные устройства
- проигрыватель Windows Media Мобильные, портативные устройства
- портативные устройства, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cbff16b293ac4ab438c1b018608497d2a61cdfa6fb727332d5b50a27de313c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745510"
---
# <a name="working-with-portable-devices"></a>Работа с портативными устройствами

в этом разделе описывается использование удаленного элемента управления проигрыватель Windows Media ActiveX для работы с портативными устройствами.

В примерах кода в этом разделе используются классы библиотеки активных шаблонов (ATL), такие как **CComPtr**.

## <a name="included-headers"></a>Включаемые заголовки

Чтобы использовать код в этом разделе, включите следующие заголовки:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>Ивмпплайер, указатель

Указатель **ивмпплайер** хранится в переменной-члене.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>Устройства хранятся в массиве

Пример кода обращается к следующей переменной члена для объявления в заголовке проекта:


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



Число устройств хранится в переменной-члене.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Получение указателя устройства

Указатель на конкретное устройство извлекается через его индекс массива с помощью кода, аналогичного следующему:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Обратите внимание, что индекс, приведенный в предыдущих примерах, не является индексом партнерства для устройства. Это индекс устройства в настраиваемом массиве устройств.

## <a name="cleaning-up"></a>Очистка

В примерах используется следующая функция для освобождения памяти в массиве устройств и для освобождения указателей интерфейса:


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



## <a name="devices-are-displayed-in-a-list-box"></a>Устройства отображаются в окне списка

Функция Жетселектеддевицеиндекс возвращает индекс устройства, выбранного пользователем в списке, с помощью следующего кода:


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>Состояние пользовательского интерфейса управляется одной функцией

Функция Сетуистате управляет пользовательским интерфейсом.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



Сведения этой функции не связаны с обсуждениями в этом разделе, но имейте в виду, что эта функция выполняет такие задачи, как включение или отключение элементов управления и изменение отображаемого текста в пользовательском интерфейсе.

Перечисление Уистате было определено следующим образом:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



Параметр *бконнектед* указывает, следует ли настраивать пользовательский интерфейс для подключенного устройства (значение true означает, что устройство подключено). Параметры *NewState* и *бконнектед* сообщают сведения, необходимые для выполнения работы функции.

В следующих разделах приводится объяснение кода примера.

-   [Перечисление устройств](enumerating-devices.md)
-   [Получение атрибутов устройства](retrieving-device-attributes.md)
-   [Отображение хода выполнения синхронизации](showing-synchronization-progress.md)
-   [Управление списками воспроизведения синхронизации](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Управление проигрывателем**](player-control-guide.md)
</dt> </dl>

 

 




