---
description: Свойство сводки безопасности передает сведения о том, следует ли открывать пакет только для чтения.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Свойство сводки безопасности
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652144"
---
# <a name="security-summary-property"></a><span data-ttu-id="722cd-103">Свойство сводки безопасности</span><span class="sxs-lookup"><span data-stu-id="722cd-103">Security Summary property</span></span>

<span data-ttu-id="722cd-104">Свойство **сводки безопасности передает сведения о** том, следует ли открывать пакет только для чтения.</span><span class="sxs-lookup"><span data-stu-id="722cd-104">The **Security Summary** property conveys whether the package should be opened as read-only.</span></span> <span data-ttu-id="722cd-105">Средство редактирования базы данных не должно изменять принудительно доступную только для чтения базу данных и выдавать предупреждение при попытке изменить базу данных, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="722cd-105">The database editing tool should not modify a read-only enforced database and should issue a warning at attempts to modify a read-only recommended database.</span></span> <span data-ttu-id="722cd-106">Следующие значения этого свойства применимы к установщик Windows файлам.</span><span class="sxs-lookup"><span data-stu-id="722cd-106">The following values of this property are applicable to Windows Installer files.</span></span>



| <span data-ttu-id="722cd-107">Значение</span><span class="sxs-lookup"><span data-stu-id="722cd-107">Value</span></span> | <span data-ttu-id="722cd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="722cd-108">Description</span></span>           |
|-------|-----------------------|
| <span data-ttu-id="722cd-109">0</span><span class="sxs-lookup"><span data-stu-id="722cd-109">0</span></span>     | <span data-ttu-id="722cd-110">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="722cd-110">No restriction</span></span>        |
| <span data-ttu-id="722cd-111">2</span><span class="sxs-lookup"><span data-stu-id="722cd-111">2</span></span>     | <span data-ttu-id="722cd-112">Рекомендуется только для чтения</span><span class="sxs-lookup"><span data-stu-id="722cd-112">Read-only recommended</span></span> |
| <span data-ttu-id="722cd-113">4</span><span class="sxs-lookup"><span data-stu-id="722cd-113">4</span></span>     | <span data-ttu-id="722cd-114">Принудительно применяется только для чтения</span><span class="sxs-lookup"><span data-stu-id="722cd-114">Read-only enforced</span></span>    |



 

<span data-ttu-id="722cd-115">Это свойство должно иметь значение рекомендуется только для чтения (2) для базы данных установки и принудительно использовать только для чтения (4) для преобразования или исправления.</span><span class="sxs-lookup"><span data-stu-id="722cd-115">This property should be set to read-only recommended (2) for an installation database and to read-only enforced (4) for a transform or patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="722cd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="722cd-116">Requirements</span></span>



| <span data-ttu-id="722cd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="722cd-117">Requirement</span></span> | <span data-ttu-id="722cd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="722cd-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="722cd-119">Версия</span><span class="sxs-lookup"><span data-stu-id="722cd-119">Version</span></span><br/> | <span data-ttu-id="722cd-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="722cd-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="722cd-121">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="722cd-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="722cd-122">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="722cd-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="722cd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="722cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="722cd-124">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="722cd-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




