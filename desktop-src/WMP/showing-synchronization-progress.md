---
title: Отображение хода выполнения синхронизации
description: Отображение хода выполнения синхронизации
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Проигрыватель Windows Media, переносные устройства
- Объектная модель проигрывателя Windows Media, переносные устройства
- Объектная модель, портативные устройства
- Элемент управления ActiveX проигрывателя Windows Media, переносные устройства
- Элемент управления ActiveX, переносные устройства
- Мобильный элемент управления ActiveX проигрывателя Windows Media, портативные устройства
- Проигрыватель Windows Media Mobile, переносные устройства
- переносные устройства, ход выполнения синхронизации
- синхронизация устройств, отображение хода выполнения
- синхронизация устройств, отображение хода выполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f109f09d4efacef620a2c21691f50cc0ac2143
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890244"
---
# <a name="showing-synchronization-progress"></a>Отображение хода выполнения синхронизации

Можно отобразить ход выполнения синхронизации пользователю. В следующем примере кода показано, как создать таймер для периодического получения текущего значения хода выполнения с помощью **ивмпсинкдевице:: Get \_ Progress**. Обратите внимание, что полученное значение Progress представляет ход выполнения для всей операции синхронизации для каждого устройства. Получение сведений о ходе синхронизации для отдельных элементов мультимедиа не поддерживается.

Чтобы определить время запуска или завершения таймера, обработайте событие **девицесинкстатечанже** . В следующем примере функции показан такой обработчик событий. Код также отображает текущее состояние синхронизации в виде текстовой строки с помощью статического элемента управления Text с именем IDC \_ синкстате.


```C++
void CMainDlg::DeviceSyncStateChange( IWMPSyncDevice * pDevice, WMPSyncState NewState )
{
    if(NULL == pDevice)
    {
        return;
    }

    HRESULT hr = E_POINTER;
    VARIANT_BOOL  vbIdentical = VARIANT_FALSE;
    // Window handle for static text control that shows the sync state.
    HWND hwndSyncStateText = GetDlgItem(IDC_SYNCSTATE); 

    // Strings to show sync state.
    const TCHAR *szSyncState[3] = {
    _T("Unknown"),
    _T("Synchronizing"),
    _T("Stopped")};

    // Get a pointer to the device the user selected in the list box.    
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]); 
    // Cache the pointer to the device that raised the event.
    CComPtr<IWMPSyncDevice> spDeviceParam(pDevice); 

    if(spDevice.p)
    {
        // Test whether the device that raised the event is the same as 
        // the one the user selected.
        hr = spDevice->isIdentical(spDeviceParam, &vbIdentical);
    }

    if(SUCCEEDED(hr) &&
        vbIdentical == VARIANT_TRUE)
    {    
        // Display the sync state.
        SendMessage(hwndSyncStateText, WM_SETTEXT, 0, (LPARAM)szSyncState[NewState]);

        switch(NewState)
        {
        case wmpssSynchronizing:
            // Start the progress timer.
            SetTimer(1, 1000, NULL);
            SetUIState(Synchronizing, TRUE);
            break;
        case wmpssStopped:
            // Stop the progress timer.
            KillTimer(1);
            // Make sure the final progress is displayed.            
            ShowProgress(GetSelectedDeviceIndex());
            SetUIState(Partnership, TRUE);
            break;      
        default:
            break;
        }
    }    
}
```



Когда таймер работает, он отправляет \_ сообщение таймера WM с интервалом в 1 секунду. Приложение обрабатывает таймер WM \_ в своем цикле обработки сообщений.

В следующем примере функции показано, как отобразить ход выполнения с помощью статического элемента управления Text (IDC \_ прогстатик) и с помощью элемента управления progress (IDC \_ синкпрог). Вызовите эту функцию в ответ на \_ сообщение таймера WM и после завершения процесса синхронизации, как показано в предыдущем примере.


```C++
STDMETHODIMP CMainDlg::ShowProgress(long lIndex)
{  
    ATLASSERT(m_ppWMPDevices);

    long lProgress = 0;
    WCHAR buffer[10]; // Buffer larger than needed to hold progress string.
    ZeroMemory(buffer, sizeof WCHAR * 10);

    // Retrieve a handle to the progress control
    HWND  hwndSyncProgressCtl = GetDlgItem(IDC_SYNCPROG); 
    // Retrieve a handle to the static control that displays 
    // progress as text.
    HWND  hwndSyncProgressText = GetDlgItem(IDC_PROGSTATIC); 

    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[lIndex]);
    
    HRESULT hr = spDevice->get_progress(&lProgress);

    // Convert progress to a string and add the percent character.
    _ltow(lProgress, buffer, 10);
    CComBSTR bstrProgress(buffer);
    bstrProgress += " %";

    // Display the text.
    ::SendMessage(hwndSyncProgressText, WM_SETTEXT, 0, (LPARAM)(LPCTSTR)COLE2T(bstrProgress));
    // Set the progress control position.
    ::SendMessage(hwndSyncProgressCtl, PBM_SETPOS, (WPARAM)(int)lProgress, 0);

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Перечисление устройств**](enumerating-devices.md)
</dt> <dt>

[**Интерфейс Ивмпсинкдевице**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Ивмпсинкдевице:: получение \_ хода выполнения**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[**Ивмпсинкдевице:: тождественно**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[**Работа с портативными устройствами**](working-with-portable-devices.md)
</dt> </dl>

 

 




