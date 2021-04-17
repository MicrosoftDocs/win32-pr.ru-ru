---
description: Рекомендуемый программный метод для установки контекстов в приложении, не поддерживающем рукописный ввод, — использование функций Сетинпутскопе для связывания контекста с полями в приложении.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Настройка контекста с помощью API-интерфейсов Сетинпутскопе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673945"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Настройка контекста с помощью API-интерфейсов Сетинпутскопе

Рекомендуемый программный метод для установки контекстов в приложении, не поддерживающем рукописный ввод, — использование функций [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) для связывания контекста с полями в приложении.

Пакет средств разработки Microsoft Windows XP Tablet PC Edition 1,7 был первой версией Microsoft Windows для предложения [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope). Windows Vista также обеспечивает поддержку этих функций. Определения **сетинпутскопе** объявляются в инпутскопе. idl и инпутскопе. h. Дополнительные сведения см. в разделе [Платформа текстовых служб](../tsf/text-services-framework.md).

[**Сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) функции — это рекомендуемый способ задания контекста для элементов управления и приложений, не поддерживающих рукописный ввод.

## <a name="common-input-scopes"></a>Общие области ввода

Используя функции [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) и определенный набор общих областей ввода, описанных в перечислении [**инпутскопе**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , можно улучшить точность распознавания распознавателей рукописного ввода Майкрософт.

> [!Note]  
> Распознаватели для английского (США), английского (Великобритания), немецкого, французского, итальянского, испанского, нидерландского и португальского языков поддерживают использование общих областей ввода с [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
