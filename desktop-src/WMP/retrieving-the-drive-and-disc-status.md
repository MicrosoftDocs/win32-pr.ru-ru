---
title: Получение состояния диска и диска
description: Получение состояния диска и диска
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-дисков, получение состояния диска и диска
- запись компакт-дисков, получение состояния диска и диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890259"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Получение состояния диска и диска

Перед запуском операции записи компакт-дисков необходимо убедиться, что выбранный дисковод компакт-дисков поддерживает операцию, которую необходимо выполнить. Например, перед вызовом [ивмпкдромбурн:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)необходимо убедиться, что компакт-диск может быть удален. В следующем коде показан пример использования [ивмпкдромбурн::](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) an, чтобы определить, поддерживается ли операция:


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Запись компакт-диска**](burning-a-cd.md)
</dt> <dt>

[**Получение интерфейса записи компакт-дисков**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Запуск процесса записи**](starting-the-burn-process.md)
</dt> <dt>

[**Стирание перезаписываемого компакт-диска**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Получение состояния записи**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




