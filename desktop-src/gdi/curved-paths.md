---
description: Кривые пути
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Кривые пути
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58018b7ef95b30c5ae2751ed963caefee7b9313ca86a8c6a2a4fee246908f8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849184"
---
# <a name="curved-paths"></a>Кривые пути

Приложение может выполнить сведение кривых в пути путем вызова функции [**флаттенпас**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) . Эта функция особенно полезна для приложений, которые соответствуют тексту на контуре контура, который содержит кривые. Чтобы вписать текст, приложение должно выполнить следующие действия:

1.  Создайте путь, по которому отображается текст.
2.  Вызовите функцию [**флаттенпас**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) , чтобы преобразовать кривые в контуре в сегменты линии.
3.  Вызовите функцию [**Multipath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) , чтобы получить эти сегменты линии.
4.  Вычислите длину каждой строки и ширину каждого символа в строке.
5.  Используйте данные ширины строки и ширины символов для размещения каждого символа вдоль кривой.

 

 



