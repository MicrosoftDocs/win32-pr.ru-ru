---
description: Пример Дмоенум
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Пример Дмоенум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262460"
---
# <a name="dmoenum-sample"></a>Пример Дмоенум

## <a name="description"></a>Описание

Этот пример приложения перечисляет все [объекты DirectX Media](directx-media-objects.md) (дмос), зарегистрированные в системе пользователя, и отображает сведения о них.

В примере используется функция [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) и интерфейс [**Иенумдмо**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) для перечисления дмос. Он использует интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) и другие интерфейсы DMO для получения сведений о каждом DMO.

## <a name="usage"></a>Использование

При запуске приложения перечисляются все установленные дмос. Если выбрана конкретная категория DMO, приложение отображает только дмос в этой категории. Чтобы просмотреть сведения о DMO, выберите DMO из списка. Приложение отображает число потоков, предпочтительные типы носителей, сервер DLL для этого DMO и другие сведения о DMO. Чтобы включить или исключить ключ дмос, установите флажок **включить ключ дмос?** .

## <a name="downloading-the-sample"></a>Загрузка образца

Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ Прочие \\ дмоенум.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры DirectShow](directshow-samples.md)
</dt> </dl>

 

 



