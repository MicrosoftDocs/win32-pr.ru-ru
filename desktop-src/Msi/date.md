---
description: Свойство Date — это текущий месяц, день и год в виде строки литерального текста в формате MM/ДД/ГГГГ.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652067"
---
# <a name="date-property"></a><span data-ttu-id="3f86d-103">Date, свойство</span><span class="sxs-lookup"><span data-stu-id="3f86d-103">Date property</span></span>

<span data-ttu-id="3f86d-104">Свойство **Date** — это текущий месяц, день и год в виде строки литерального текста в формате mm/дд/гггг.</span><span class="sxs-lookup"><span data-stu-id="3f86d-104">The **Date** property is the current month, day, and year as a string of literal text in the format MM/DD/YYYY.</span></span> <span data-ttu-id="3f86d-105">Например, дата 22 июня 2005 может быть представлена в виде 06/22/2005.</span><span class="sxs-lookup"><span data-stu-id="3f86d-105">For example, the date June 22, 2005 can represented as "06/22/2005".</span></span> <span data-ttu-id="3f86d-106">Формат значения зависит от языкового стандарта пользователя и имеет формат, полученный с помощью [**жетдатеформат**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) с \_ параметром Date шортдате.</span><span class="sxs-lookup"><span data-stu-id="3f86d-106">The format of the value depends upon the user's locale, and is the format obtained using [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) with the DATE\_SHORTDATE option.</span></span> <span data-ttu-id="3f86d-107">Значение этого свойства задается установщик Windows, а не автором пакета.</span><span class="sxs-lookup"><span data-stu-id="3f86d-107">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f86d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f86d-108">Remarks</span></span>

<span data-ttu-id="3f86d-109">Поскольку это текстовая строка, ее нельзя использовать в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="3f86d-109">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f86d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="3f86d-110">Requirements</span></span>



| <span data-ttu-id="3f86d-111">Требование</span><span class="sxs-lookup"><span data-stu-id="3f86d-111">Requirement</span></span> | <span data-ttu-id="3f86d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3f86d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f86d-113">Версия</span><span class="sxs-lookup"><span data-stu-id="3f86d-113">Version</span></span><br/> | <span data-ttu-id="3f86d-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f86d-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3f86d-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3f86d-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3f86d-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f86d-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3f86d-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3f86d-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f86d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3f86d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f86d-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f86d-119">Properties</span></span>](properties.md)
</dt> </dl>

 

