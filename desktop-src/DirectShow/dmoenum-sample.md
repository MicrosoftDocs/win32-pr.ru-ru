---
description: Пример Дмоенум
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Пример Дмоенум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fc51cc45ad879ccbc5ccd232b782e4b9f5511071d8d2492c135efcb322969c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079204"
---
# <a name="dmoenum-sample"></a>Пример Дмоенум

## <a name="description"></a>Описание

Этот пример приложения перечисляет все [объекты DirectX Media](directx-media-objects.md) (дмос), зарегистрированные в системе пользователя, и отображает сведения о них.

В примере используется функция [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) и интерфейс [**Иенумдмо**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) для перечисления дмос. он использует интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) и другие интерфейсы DMO для получения сведений о каждой DMO.

## <a name="usage"></a>Использование

При запуске приложения перечисляются все установленные дмос. если выбрана определенная категория DMO, приложение отображает только дмос в этой категории. чтобы просмотреть сведения о DMO, выберите DMO из списка. приложение отображает число потоков, предпочтительные типы носителей, сервер DLL для этой DMO и другие сведения о DMO. Чтобы включить или исключить ключ дмос, установите флажок **включить ключ дмос?** .

## <a name="downloading-the-sample"></a>Загрузка образца

чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ прочие \\ дмоенум.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Регистрируют](directshow-samples.md)
</dt> </dl>

 

 



