---
title: Рекомендации по пользовательскому интерфейсу для расширений классов модуля поддержки NDF
description: При создании вспомогательного класса необходимо создать текст, чтобы помочь пользователю понять причину инцидента и возможные действия по восстановлению, которые можно предпринять.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104335408"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a><span data-ttu-id="bfbae-103">Рекомендации по пользовательскому интерфейсу для расширений классов модуля поддержки NDF</span><span class="sxs-lookup"><span data-stu-id="bfbae-103">UI guidelines for NDF helper class extensions</span></span>

<span data-ttu-id="bfbae-104">При создании вспомогательного класса необходимо создать текст, чтобы помочь пользователю понять причину инцидента и возможные действия по восстановлению, которые можно предпринять.</span><span class="sxs-lookup"><span data-stu-id="bfbae-104">When building your helper class, you will need to create text to help the user understand the cause of an incident and the possible repair steps which can be taken.</span></span>

## <a name="root-cause-and-repair"></a><span data-ttu-id="bfbae-105">Основная причина и восстановление</span><span class="sxs-lookup"><span data-stu-id="bfbae-105">Root Cause and Repair</span></span>

<span data-ttu-id="bfbae-106">При возникновении инцидента появляется диалоговое окно, сообщающее пользователю о том, что произошло.</span><span class="sxs-lookup"><span data-stu-id="bfbae-106">When an incident occurs, a dialog box will appear to inform the user about what has happened.</span></span> <span data-ttu-id="bfbae-107">Созданный текст будет отображаться в двух отдельных областях.</span><span class="sxs-lookup"><span data-stu-id="bfbae-107">The text that you create will appear in two separate areas.</span></span>

-   <span data-ttu-id="bfbae-108">**Основная причина**: краткое описание причины проблемы.</span><span class="sxs-lookup"><span data-stu-id="bfbae-108">**Root Cause**: A brief description of the cause of the issue.</span></span> <span data-ttu-id="bfbae-109">Содержит сведения, помогающие администратору или расширенному пользователю устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="bfbae-109">Contains information to help an administrator or advanced user troubleshoot the problem.</span></span>
-   <span data-ttu-id="bfbae-110">**Исправление**: раскрывает основную причину, чтобы предоставить дополнительные сведения о действиях, которые может выполнить пользователь, не прибегая к слишком длине.</span><span class="sxs-lookup"><span data-stu-id="bfbae-110">**Repair**: Expands on the root cause to provide more details about the steps that a user can take, without getting too lengthy.</span></span>

<span data-ttu-id="bfbae-111">Каждая основная причина или восстановление должны иметь заголовок и описание.</span><span class="sxs-lookup"><span data-stu-id="bfbae-111">Each root cause or repair should have a title and a description.</span></span> <span data-ttu-id="bfbae-112">Весь текст перед первым \\ символом "n" будет использован для заголовка.</span><span class="sxs-lookup"><span data-stu-id="bfbae-112">All text before the first "\\n" character will be used for the title.</span></span> <span data-ttu-id="bfbae-113">В описании будет использоваться весь текст, следующий за первым \\ символом "n" (включая все последующие разрывы строк).</span><span class="sxs-lookup"><span data-stu-id="bfbae-113">All text following the first "\\n" character (including any subsequent line breaks) will be used for the description.</span></span>

## <a name="title-guidelines"></a><span data-ttu-id="bfbae-114">Рекомендации по названиям</span><span class="sxs-lookup"><span data-stu-id="bfbae-114">Title Guidelines</span></span>

<span data-ttu-id="bfbae-115">Название основной причины или восстановления должно соответствовать следующим рекомендациям:</span><span class="sxs-lookup"><span data-stu-id="bfbae-115">The title of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="bfbae-116">Длина должна составлять 128 символов или меньше.</span><span class="sxs-lookup"><span data-stu-id="bfbae-116">Must be 128 characters or fewer.</span></span> <span data-ttu-id="bfbae-117">(рекомендуется не более 40 символов.)</span><span class="sxs-lookup"><span data-stu-id="bfbae-117">(40 characters or less is recommended.)</span></span>
-   <span data-ttu-id="bfbae-118">Не должно заканчиваться точкой.</span><span class="sxs-lookup"><span data-stu-id="bfbae-118">Should not end with a period.</span></span>

## <a name="description-guidelines"></a><span data-ttu-id="bfbae-119">Рекомендации по описанию</span><span class="sxs-lookup"><span data-stu-id="bfbae-119">Description Guidelines</span></span>

<span data-ttu-id="bfbae-120">Описание основной причины или восстановления должно соответствовать следующим рекомендациям:</span><span class="sxs-lookup"><span data-stu-id="bfbae-120">The description of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="bfbae-121">Длина должна составлять 512 символов или меньше.</span><span class="sxs-lookup"><span data-stu-id="bfbae-121">Must be 512 characters or fewer.</span></span>
-   <span data-ttu-id="bfbae-122">Каждое предложение должно заканчиваться точкой.</span><span class="sxs-lookup"><span data-stu-id="bfbae-122">Each sentence should end with a period.</span></span>
-   <span data-ttu-id="bfbae-123">Символ " \\ n" может использоваться для создания разрыва строки в описании.</span><span class="sxs-lookup"><span data-stu-id="bfbae-123">The "\\n" character may be used to create a line break in the description.</span></span>

 

 




