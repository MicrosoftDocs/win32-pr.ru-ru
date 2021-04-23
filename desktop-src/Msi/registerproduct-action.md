---
description: Действие Регистерпродукт регистрирует сведения о продукте с помощью установщика и с помощью команды "Установка и удаление программ". Кроме того, это действие сохраняет пакет установщик Windows базы данных на локальном компьютере.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Действие Регистерпродукт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673666"
---
# <a name="registerproduct-action"></a><span data-ttu-id="11cd2-104">Действие Регистерпродукт</span><span class="sxs-lookup"><span data-stu-id="11cd2-104">RegisterProduct Action</span></span>

<span data-ttu-id="11cd2-105">Действие Регистерпродукт регистрирует сведения о продукте с помощью установщика и с помощью команды "Установка и удаление программ".</span><span class="sxs-lookup"><span data-stu-id="11cd2-105">The RegisterProduct action registers the product information with the installer and with Add/Remove Programs.</span></span> <span data-ttu-id="11cd2-106">Кроме того, это действие сохраняет пакет установщик Windows базы данных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="11cd2-106">Additionally, this action stores the Windows Installer database package on the local computer.</span></span>

<span data-ttu-id="11cd2-107">Действие Регистерпродукт настраивает элементы управления, отображаемые в окне Установка и удаление программ на панели управления.</span><span class="sxs-lookup"><span data-stu-id="11cd2-107">The RegisterProduct action configures the controls displayed by the Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="11cd2-108">Дополнительные сведения см. в разделе [Настройка установки и удаления программ с помощью установщик Windows](configuring-add-remove-programs-with-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="11cd2-108">For more information, see [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="11cd2-109">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="11cd2-109">Sequence Restrictions</span></span>

<span data-ttu-id="11cd2-110">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="11cd2-110">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="11cd2-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="11cd2-111">ActionData Messages</span></span>



| <span data-ttu-id="11cd2-112">Поле</span><span class="sxs-lookup"><span data-stu-id="11cd2-112">Field</span></span> | <span data-ttu-id="11cd2-113">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="11cd2-113">Description of action data</span></span>            |
|-------|---------------------------------------|
| <span data-ttu-id="11cd2-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="11cd2-114">\[1\]</span></span> | <span data-ttu-id="11cd2-115">Сведения о зарегистрированном продукте.</span><span class="sxs-lookup"><span data-stu-id="11cd2-115">Information about registered product.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11cd2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11cd2-116">Remarks</span></span>

<span data-ttu-id="11cd2-117">Действие Регистерпродукт не выполняется во время установки до точки административной установки.</span><span class="sxs-lookup"><span data-stu-id="11cd2-117">The RegisterProduct action is not performed during installation to an administrative installation point.</span></span>

 

 



