---
title: DirectComposition
description: В этом разделе объясняется назначение Microsoft DirectComposition, определяются требования к времени выполнения и описывается, как эффективно использовать Microsoft DirectComposition.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1b13dbd0ee4893f1b208cd88d7fd1251b5fb7ece2400b7e0b195e84865b2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985414"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> для приложений на Windows 10 рекомендуется использовать интерфейсы api Windows. UI. компоновки вместо DirectComposition. Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Назначение

Microsoft DirectComposition — это Windows компонент, который позволяет создавать высокопроизводительные растровые изображения с помощью преобразований, эффектов и анимации. Разработчики приложений могут использовать API DirectComposition для создания визуально привлекательных пользовательских интерфейсов с плавными анимированными переходами от одного визуального элемента к другому.

DirectComposition обеспечивает широкие и жидкие переходы за счет высокой частоты кадров, использования графического оборудования и работы независимо от потока пользовательского интерфейса. DirectComposition может принимать растровое содержимое, рисуемое различными библиотеками отрисовки, включая точечные рисунки Microsoft DirectX, и растровые изображения, отображаемые в окне (точечные рисунки HWND). Кроме того, DirectComposition поддерживает разнообразные преобразования, такие как двухмерные преобразования 2D и трехмерные перспективы, а также базовые эффекты, такие как обрезка и непрозрачность.

DirectComposition предназначен для упрощения процесса составления [*визуальных элементов*](directcomposition-glossary.md) и создания анимированных переходов. Если приложение уже содержит код подготовки к просмотру или уже использует рекомендованный API DirectX, достаточно выполнить минимальный объем работы, чтобы эффективно использовать DirectComposition.

## <a name="developer-audience"></a>Аудитория разработчиков

API DirectComposition предназначен для опытных и высокопроизводительных графических разработчиков, знающих C/C++, имеющих четкое представление об объектной модели компонентов (COM) и знакомых с Windows концепциями программирования.

## <a name="run-time-requirements"></a>Требования к среде выполнения

DirectComposition был введен в Windows 8. Он включается в 32-разрядные, 64-битные и процессорные платформы ARM.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                       | Описание                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Зачем использовать DirectComposition?](why-use-directcomposition-.md)<br/>     | В этом разделе описываются возможности и преимущества DirectComposition. <br/>                                                                           |
| [Как использовать DirectComposition](how-to-use-directcomposition.md)<br/> | В этом разделе описываются рекомендации по использованию API DirectComposition и демонстрируется использование API для выполнения нескольких распространенных задач. <br/> |
| [Основные понятия DirectComposition](directcomposition-concepts.md)<br/>     | Этот раздел содержит общие сведения о DirectComposition.<br/>                                                                                   |
| [Справочник по DirectComposition](reference.md)<br/>                     | В этом разделе содержатся подробные справочные сведения об элементах, которые составляют API DirectComposition.<br/>                                       |
| [Примеры DirectComposition](directcomposition-code-samples.md)<br/>  | В следующих примерах приложений показано, как использовать API DirectComposition и продемонстрировать его возможности. <br/>                                      |
| [Глоссарий DirectComposition](directcomposition-glossary.md)<br/>     | В этом разделе определяются термины DirectComposition. <br/>                                                                                                        |



 

 

 





