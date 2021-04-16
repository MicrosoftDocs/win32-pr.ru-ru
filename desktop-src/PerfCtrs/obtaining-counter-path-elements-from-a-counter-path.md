---
description: Чтобы получить элементы пути, вызовите функцию Пдхпарсекаунтерпас. Функция анализирует элементы пути счетчика и возвращает их в \_ \_ структуре элементов пути счетчика PDH \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Получение элементов пути счетчика из пути счетчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663223"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Получение элементов пути счетчика из пути счетчика

Чтобы получить элементы пути, вызовите функцию [**пдхпарсекаунтерпас**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) . Функция анализирует элементы пути счетчика и возвращает их в структуре [**\_ \_ \_ элементов пути счетчика PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .

Если имеется сложное имя экземпляра (которое содержит родительский экземпляр и индекс экземпляра), можно вызвать функцию [**пдхпарсеинстанценаме**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) для извлечения имени экземпляра, индекса экземпляра и имени родителя.

 

 



