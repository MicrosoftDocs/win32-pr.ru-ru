---
description: Функция QueryContextAttributes (Digest) предоставляет сведения о текущих параметрах контекста безопасности.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Запрос атрибутов контекста безопасности дайджеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998404"
---
# <a name="querying-digest-security-context-attributes"></a><span data-ttu-id="52249-103">Запрос атрибутов контекста безопасности дайджеста</span><span class="sxs-lookup"><span data-stu-id="52249-103">Querying Digest Security Context Attributes</span></span>

<span data-ttu-id="52249-104">Функция [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) предоставляет сведения о текущих параметрах [*контекста безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="52249-104">The [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) function provides information about the current settings of a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="52249-105">Microsoft Digest поддерживает запросы к следующим атрибутам контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="52249-105">Microsoft Digest supports querying the following security context attributes.</span></span>



| <span data-ttu-id="52249-106">attribute</span><span class="sxs-lookup"><span data-stu-id="52249-106">Attribute</span></span>                   | <span data-ttu-id="52249-107">Описание</span><span class="sxs-lookup"><span data-stu-id="52249-107">Description</span></span>                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52249-108">\_ \_ сведения о ключе SECPKG attr \_</span><span class="sxs-lookup"><span data-stu-id="52249-108">SECPKG\_ATTR\_KEY\_INFO</span></span>     | <span data-ttu-id="52249-109">Сведения, относящиеся к используемым алгоритмам подписывания и шифрования.</span><span class="sxs-lookup"><span data-stu-id="52249-109">Information relating to the signing and encryption algorithms in use.</span></span>                                                                                                                                   |
| <span data-ttu-id="52249-110">\_ \_ сведения о пакете attr SECPKG \_</span><span class="sxs-lookup"><span data-stu-id="52249-110">SECPKG\_ATTR\_PACKAGE\_INFO</span></span> | <span data-ttu-id="52249-111">Общие сведения, относящиеся к Microsoft Digest, такие как максимальный размер маркера, разрешенный [*пакетом безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="52249-111">General information pertaining to Microsoft Digest, such as the maximum token size permitted by the [*security package*](../secgloss/s-gly.md).</span></span> |
| <span data-ttu-id="52249-112">\_размеры SECPKG attr \_</span><span class="sxs-lookup"><span data-stu-id="52249-112">SECPKG\_ATTR\_SIZES</span></span>         | <span data-ttu-id="52249-113">Максимальный размер, разрешенный для данных, связанных с сообщениями, таких как подписи.</span><span class="sxs-lookup"><span data-stu-id="52249-113">The maximum sizes permitted for message-related data such as signatures.</span></span>                                                                                                                                |



 

 

 
