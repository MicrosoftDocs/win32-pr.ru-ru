---
description: Рекомендуемый программный метод для установки контекстов в приложении, не поддерживающем рукописный ввод, — использование функций Сетинпутскопе для связывания контекста с полями в приложении.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Настройка контекста с помощью API-интерфейсов Сетинпутскопе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0abe9992e4a4ee81190fdee022b11f443592e05d7c99f9a5e69d0a200f63ecbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708154"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Настройка контекста с помощью API-интерфейсов Сетинпутскопе

Рекомендуемый программный метод для установки контекстов в приложении, не поддерживающем рукописный ввод, — использование функций [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) для связывания контекста с полями в приложении.

пакет средств разработки microsoft Windows XP Tablet PC Edition 1,7 был первой версией microsoft Windows для предложения [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope). Windows Vista также обеспечивает поддержку этих функций. Определения **сетинпутскопе** объявляются в инпутскопе. idl и инпутскопе. h. Дополнительные сведения см. в разделе [Платформа текстовых служб](../tsf/text-services-framework.md).

[**Сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) функции — это рекомендуемый способ задания контекста для элементов управления и приложений, не поддерживающих рукописный ввод.

## <a name="common-input-scopes"></a>Общие области ввода

Используя функции [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) и определенный набор общих областей ввода, описанных в перечислении [**инпутскопе**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , можно улучшить точность распознавания распознавателей рукописного ввода Майкрософт.

> [!Note]  
> Распознаватели для английского (США), английского (Великобритания), немецкого, французского, итальянского, испанского, нидерландского и португальского языков поддерживают использование общих областей ввода с [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
