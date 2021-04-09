---
title: Объект свойств входного носителя
description: Объект свойств входного носителя
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK, объекты свойств входного носителя
- Расширенный системный формат (ASF), объекты свойств входного носителя
- ASF (Расширенный системный формат), объекты свойств входного носителя
- объекты, объекты свойств входных данных мультимедиа
- объекты свойств входного носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890228"
---
# <a name="input-media-properties-object"></a>Объект свойств входного носителя

Входной объект свойств носителя, созданный объектом Writer, поддерживает следующие интерфейсы. Доступ к этим интерфейсам осуществляется путем вызова **QueryInterface** в одном из интерфейсов объекта модуля записи.



| Интерфейс                                        | Описание                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Извлекает свойства входного потока.                                                               |
| [**ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Используется в качестве базового интерфейса для других интерфейсов свойств мультимедиа (входные, выходные и видео).             |
| [**ивмвидеомедиапропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Управляет свойствами потока видео. Это необязательный интерфейс, доступный только для потоков видео. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объекты**](objects.md)
</dt> <dt>

[**Объект модуля записи**](writer-object.md)
</dt> </dl>

 

 




