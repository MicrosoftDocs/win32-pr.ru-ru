---
title: Получение состояния диска и диска
description: Получение состояния диска и диска
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- проигрыватель Windows Media, запись компакт-дисков
- проигрыватель Windows Media объектной модели, запись компакт-диска
- Объектная модель, запись компакт-диска
- проигрыватель Windows Media ActiveX управления, запись компакт-дисков
- ActiveX управления, запись компакт-дисков
- проигрыватель Windows Media мобильный ActiveX элемент управления, запись компакт-дисков
- проигрыватель Windows Media Мобильные устройства, запись компакт-дисков
- Запись компакт-дисков, получение состояния диска и диска
- запись компакт-дисков, получение состояния диска и диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664315972158b4cf68e7f766f98be095a27d7fa8496f983305cc6baaafe784d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746276"
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



## <a name="related-topics"></a>Связанные темы

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

 

 




