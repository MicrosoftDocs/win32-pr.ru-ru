---
description: Функции установщик Windows, которые возвращают данные в предоставленном пользователем виде, не должны вызываться со значением NULL в качестве значения для указателя.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Передача значений NULL в функции установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650637"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a><span data-ttu-id="0ffd1-103">Передача значения NULL в качестве аргумента функций установщик Windows</span><span class="sxs-lookup"><span data-stu-id="0ffd1-103">Passing null as the Argument of Windows Installer Functions</span></span>

<span data-ttu-id="0ffd1-104">Функции установщик Windows, которые возвращают данные в предоставленном пользователем виде, не должны вызываться со значением NULL в качестве значения для указателя.</span><span class="sxs-lookup"><span data-stu-id="0ffd1-104">Windows Installer functions that return data in a user provided–memory location should not be called with null as the value for the pointer.</span></span> <span data-ttu-id="0ffd1-105">Эти функции возвращают строку или возвращают данные в виде целочисленных указателей, но возвращают непротиворечивые значения при передаче значения NULL в качестве аргумента Output.</span><span class="sxs-lookup"><span data-stu-id="0ffd1-105">These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument.</span></span>

<span data-ttu-id="0ffd1-106">Не передавайте значение NULL в качестве значения аргумента Output для любой из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="0ffd1-106">Do not pass Null as the value of the output argument for any of the following functions:</span></span>

[<span data-ttu-id="0ffd1-107">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-107">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[<span data-ttu-id="0ffd1-108">**мсирекорджетстринг**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-108">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[<span data-ttu-id="0ffd1-109">**мсиформатрекорд**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-109">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[<span data-ttu-id="0ffd1-110">**мсижетсаурцепас**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[<span data-ttu-id="0ffd1-111">**мсижеттаржетпас**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[<span data-ttu-id="0ffd1-112">**мсижетфеатурестате**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-112">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="0ffd1-113">**мсивиевжетеррор**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-113">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[<span data-ttu-id="0ffd1-114">**мсисуммаринфожетпроперти**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-114">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[<span data-ttu-id="0ffd1-115">**мсиевалуатекондитион**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-115">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[<span data-ttu-id="0ffd1-116">**мсижетфеатурекост**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-116">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="0ffd1-117">**мсижетфеатурестате**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-117">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="0ffd1-118">**мсижеткомпонентстате**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-118">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[<span data-ttu-id="0ffd1-119">**мсижетфеатурекост**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-119">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="0ffd1-120">**мсижетфеатуревалидстатес**</span><span class="sxs-lookup"><span data-stu-id="0ffd1-120">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



