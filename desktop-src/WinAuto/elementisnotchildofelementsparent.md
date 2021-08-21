---
title: елементиснотчилдофелементспарент
description: елементиснотчилдофелементспарент
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906e9debd379950a7fc8ba2fa8faf5795cd21db8d1d82c465d5c8ff410082347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829542"
---
# <a name="elementisnotchildofelementsparent"></a>елементиснотчилдофелементспарент

## <a name="text"></a>Текст

Элемент не является дочерним элементом родительского элемента

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

При вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочернего элемента, возвращенного [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (с помощью \_ констант навигации навдир FIRSTCHILD или навдир \_ LASTCHILD), возвращаемый родительский элемент не соответствует родительскому элементу, указанному в вызове **аккнавигате** .

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




