---
description: Если для этой системной политики "на пользователя" задано значение &\# 0034; 1&\# 0034;, пользователи и администраторы, выполняющие установку одного продукта, не смогут использовать диалоговое окно обзора для просмотра источников мультимедиа, таких как CD-ROM, для источников других устанавливаемых продуктов.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: дисаблемедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999852"
---
# <a name="disablemedia"></a><span data-ttu-id="9d79d-103">дисаблемедиа</span><span class="sxs-lookup"><span data-stu-id="9d79d-103">DisableMedia</span></span>

<span data-ttu-id="9d79d-104">Если для этой [системной политики](system-policy.md) "на пользователя" задано значение "1", пользователи и администраторы, выполняющие установку одного продукта на обслуживание, не смогут использовать диалоговое окно "Обзор" для просмотра источников мультимедиа, таких как CD-ROM, для источников других устанавливаемых продуктов.</span><span class="sxs-lookup"><span data-stu-id="9d79d-104">If this per-user [system policy](system-policy.md) is set to "1", users and administrators running a maintenance installation of one product are prevented from using the Browse Dialog to browse media sources, such as CD-ROM, for the sources of other installable products.</span></span> <span data-ttu-id="9d79d-105">Просмотр других продуктов запрещается независимо от того, выполняется ли установка с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="9d79d-105">Browsing for other products is prevented regardless of whether the installation is done with elevated privileges.</span></span> <span data-ttu-id="9d79d-106">Пользователь по-прежнему может переустановить продукт с носителя, если у пользователя есть правильно помеченный источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9d79d-106">It is still possible for the user to reinstall the product from media if the user has a correctly labeled media source.</span></span>

## <a name="registry-key"></a><span data-ttu-id="9d79d-107">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="9d79d-107">Registry Key</span></span>

<span data-ttu-id="9d79d-108">**HKey \_ Текущие \_ политики пользовательского** \\ **программного обеспечения** \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="9d79d-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="9d79d-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9d79d-109">Data Type</span></span>

<span data-ttu-id="9d79d-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9d79d-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="9d79d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d79d-111">Remarks</span></span>

<span data-ttu-id="9d79d-112">Обратите внимание, что свойство [**дисаблемедиа**](-disablemedia.md) отличается от влияния политики дисаблемедиа.</span><span class="sxs-lookup"><span data-stu-id="9d79d-112">Note that the [**DISABLEMEDIA**](-disablemedia.md) property has a different effect than the DisableMedia policy.</span></span> <span data-ttu-id="9d79d-113">Установка системной политики Дисаблемедиа отключает только просмотр источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9d79d-113">Setting the DisableMedia system policy, only disables browsing to media sources.</span></span> <span data-ttu-id="9d79d-114">Если задать свойство **дисаблемедиа** , установщик не сможет зарегистрировать какой-либо источник мультимедиа, например компакт-диск, в качестве допустимого источника для продукта.</span><span class="sxs-lookup"><span data-stu-id="9d79d-114">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="9d79d-115">Однако если обзор включен, пользователь по-прежнему может перейти к источнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9d79d-115">If browsing is enabled however, a user may still browse to a media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d79d-116">См. также</span><span class="sxs-lookup"><span data-stu-id="9d79d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d79d-117">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="9d79d-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



