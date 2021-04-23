---
description: Установщик задает для свойства CommonFiles64Folder полный путь к стандартной папке общих файлов 64-bit. Для существующего свойства Коммонфилесфолдер задается соответствующая 32-разрядная папка.
ms.assetid: 6730170a-0f73-4a84-b3fb-bd15c72917c7
title: CommonFiles64Folder, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44a6720e609cfa79cd0e4adbfd5136c7a92a5ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651951"
---
# <a name="commonfiles64folder-property"></a><span data-ttu-id="b2dbc-104">CommonFiles64Folder, свойство</span><span class="sxs-lookup"><span data-stu-id="b2dbc-104">CommonFiles64Folder property</span></span>

<span data-ttu-id="b2dbc-105">Установщик задает для свойства **CommonFiles64Folder** полный путь к стандартной папке общих файлов 64-bit.</span><span class="sxs-lookup"><span data-stu-id="b2dbc-105">The installer sets the **CommonFiles64Folder** property to the full path of the predefined 64-bit Common Files folder.</span></span> <span data-ttu-id="b2dbc-106">Для существующего свойства [**коммонфилесфолдер**](commonfilesfolder.md) задается соответствующая 32-разрядная папка.</span><span class="sxs-lookup"><span data-stu-id="b2dbc-106">The existing [**CommonFilesFolder**](commonfilesfolder.md) property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2dbc-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2dbc-107">Remarks</span></span>

<span data-ttu-id="b2dbc-108">Установщик задает это свойство для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="b2dbc-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="b2dbc-109">Это свойство не используется в 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="b2dbc-109">This property is not used on 32-bit Windows.</span></span> <span data-ttu-id="b2dbc-110">При использовании 64-разрядной версии Windows значение может быть "C: \\ Program Files \\ Common Files".</span><span class="sxs-lookup"><span data-stu-id="b2dbc-110">When using 64-bit Windows, the value may be "C:\\Program Files\\Common Files".</span></span>

## <a name="requirements"></a><span data-ttu-id="b2dbc-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b2dbc-111">Requirements</span></span>



| <span data-ttu-id="b2dbc-112">Требование</span><span class="sxs-lookup"><span data-stu-id="b2dbc-112">Requirement</span></span> | <span data-ttu-id="b2dbc-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dbc-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2dbc-114">Версия</span><span class="sxs-lookup"><span data-stu-id="b2dbc-114">Version</span></span><br/> | <span data-ttu-id="b2dbc-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b2dbc-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b2dbc-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2dbc-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b2dbc-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2dbc-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b2dbc-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b2dbc-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2dbc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b2dbc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2dbc-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="b2dbc-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




