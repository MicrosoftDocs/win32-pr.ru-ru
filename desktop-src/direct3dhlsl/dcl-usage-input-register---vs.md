---
title: Ввод dcl_usage (SM1, SM2, SM3-VS ASM)
description: Объявите ассоциацию между использованием элемента вершины и индексом использования для входного регистра шейдера вершин.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129691"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>\_входные данные об использовании дкл (SM1, SM2, SM3-VS ASM)

Объявите ассоциацию между использованием элемента вершины и индексом использования для входного регистра шейдера вершин.

## <a name="syntax"></a>Синтаксис

\_ \[ индекс использования дкл \_ Usage \] v\#



 

Где:

-   \_Использование дкл определяет, как будут использоваться данные регистра. Это то же значение, что и члены [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) без префикса D3DDECLUSAGE.
-   \_индекс использования — это необязательный целочисленный индекс от 0 до 15. Он изменяет данные об использовании. Индекс соответствует индексу использования в объявлении вершины. См. [Описание вершины (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration). Индекс добавляется к значению использования (дкл \_ Usage) без пробелов. Если он не указан, предполагается, что он равен 0.
-   v \# является [входным регистром](dx9-graphics-reference-asm-vs-registers-input.md).

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_Использование дкл             | x    | x    | x    | x     | x    | x     |



 

Все \_ инструкции по использованию дкл должны располагаться перед первой исполняемой инструкцией.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
