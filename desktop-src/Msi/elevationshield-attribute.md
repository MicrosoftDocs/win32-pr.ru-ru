---
description: Этот атрибут добавляет значок повышения прав контроля учетных записей (UAC) (значок щита) в элемент управления "Кнопка".
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Атрибут Елеватионшиелд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156635"
---
# <a name="elevationshield-attribute"></a><span data-ttu-id="10f33-103">Атрибут Елеватионшиелд</span><span class="sxs-lookup"><span data-stu-id="10f33-103">ElevationShield Attribute</span></span>

<span data-ttu-id="10f33-104">Этот атрибут добавляет значок повышения прав контроля [*учетных записей*](u-gly.md) (UAC) (значок щита) в [элемент управления "кнопка](pushbutton-control.md)".</span><span class="sxs-lookup"><span data-stu-id="10f33-104">This attribute adds the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon) to the [PushButton control](pushbutton-control.md).</span></span>

<span data-ttu-id="10f33-105">Если этот бит задан, а установка еще не запущена с [*повышенными*](e-gly.md) привилегиями, элемент управления "Кнопка" создается с помощью значка повышения прав контроля [*учетных записей*](u-gly.md) (UAC) (значок щита).</span><span class="sxs-lookup"><span data-stu-id="10f33-105">If this bit is set, and the installation is not yet running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon).</span></span>

<span data-ttu-id="10f33-106">Если этот бит задан, а установка уже запущена с [*повышенными*](e-gly.md) привилегиями, то элемент управления "Кнопка" создается с использованием других атрибутов значков.</span><span class="sxs-lookup"><span data-stu-id="10f33-106">If this bit is set, and the installation is already running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the other icon attributes.</span></span>

<span data-ttu-id="10f33-107">Если этот бит не задан, элемент управления "Кнопка" создается с использованием других атрибутов значка.</span><span class="sxs-lookup"><span data-stu-id="10f33-107">If this bit is not set, the pushbutton control is created using the other icon attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="10f33-108">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="10f33-108">Valid Controls</span></span>

[<span data-ttu-id="10f33-109">PushButton</span><span class="sxs-lookup"><span data-stu-id="10f33-109">PushButton</span></span>](pushbutton-control.md)

## <a name="value"></a><span data-ttu-id="10f33-110">Значение</span><span class="sxs-lookup"><span data-stu-id="10f33-110">Value</span></span>



| <span data-ttu-id="10f33-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="10f33-111">Decimal</span></span> | <span data-ttu-id="10f33-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="10f33-112">Hexadecimal</span></span> | <span data-ttu-id="10f33-113">Константа</span><span class="sxs-lookup"><span data-stu-id="10f33-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="10f33-114">8388608</span><span class="sxs-lookup"><span data-stu-id="10f33-114">8388608</span></span> | <span data-ttu-id="10f33-115">0x00800000</span><span class="sxs-lookup"><span data-stu-id="10f33-115">0x00800000</span></span>  | <span data-ttu-id="10f33-116">**мсидбконтролаттрибутеселеватионшиелд**</span><span class="sxs-lookup"><span data-stu-id="10f33-116">**msidbControlAttributesElevationShield**</span></span> |



 

 

 



