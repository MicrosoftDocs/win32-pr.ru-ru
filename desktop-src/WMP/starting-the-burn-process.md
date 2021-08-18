---
title: Запуск процесса записи
description: Запуск процесса записи
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- проигрыватель Windows Media, запись компакт-дисков
- проигрыватель Windows Media объектной модели, запись компакт-диска
- Объектная модель, запись компакт-диска
- проигрыватель Windows Media ActiveX управления, запись компакт-дисков
- ActiveX управления, запись компакт-дисков
- проигрыватель Windows Media мобильный ActiveX элемент управления, запись компакт-дисков
- проигрыватель Windows Media Мобильные устройства, запись компакт-дисков
- Запись компакт-дисков, запуск процесса записи
- запись компакт-дисков, запуск процесса записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f5620ba8fa6ab911cf0fd594fd27f139b5061d1383575f861dadfec45dabbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995084"
---
# <a name="starting-the-burn-process"></a>Запуск процесса записи

Перед началом записи необходимо назначить список воспроизведения. Используйте [ивмпкдромбурн::p UT \_ бурнплайлист](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) , чтобы указать список воспроизведения для записи.


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



Дополнительные сведения об использовании списков воспроизведения см. в разделе [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Чтобы начать операцию записи, вызовите метод [ивмпкдромбурн:: стартбурн](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



Можно прерывать операцию записи путем вызова [ивмпкдромбурн:: стопбурн](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Запись компакт-диска**](burning-a-cd.md)
</dt> <dt>

[**Получение интерфейса записи компакт-дисков**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Стирание перезаписываемого компакт-диска**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Получение состояния диска и диска**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Получение состояния записи**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




