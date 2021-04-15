---
description: Установщик задает для свойства Темпфолдер полный путь к папке Temp. Авторам не нужно задавать свойство Темпфолдер.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Темпфолдер, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651643"
---
# <a name="tempfolder-property"></a><span data-ttu-id="1e1d9-103">Темпфолдер, свойство</span><span class="sxs-lookup"><span data-stu-id="1e1d9-103">TempFolder property</span></span>

<span data-ttu-id="1e1d9-104">Установщик задает для свойства **темпфолдер** полный путь к папке Temp.</span><span class="sxs-lookup"><span data-stu-id="1e1d9-104">The installer sets the **TempFolder** property to the full path to the Temp folder.</span></span>

<span data-ttu-id="1e1d9-105">Авторам не нужно задавать свойство **темпфолдер** .</span><span class="sxs-lookup"><span data-stu-id="1e1d9-105">Authors should not need to set the **TempFolder** property.</span></span> <span data-ttu-id="1e1d9-106">Установщик Windows использует функцию [**жеттемппас**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) для получения пути к каталогу, предназначенному для временных файлов, и для задания этого свойства.</span><span class="sxs-lookup"><span data-stu-id="1e1d9-106">Windows Installer uses the [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files and to set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e1d9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e1d9-107">Remarks</span></span>

<span data-ttu-id="1e1d9-108">Общее значение для этого свойства — C: \\ TEMP.</span><span class="sxs-lookup"><span data-stu-id="1e1d9-108">A common value for this property is C:\\Temp.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e1d9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1e1d9-109">Requirements</span></span>



| <span data-ttu-id="1e1d9-110">Требование</span><span class="sxs-lookup"><span data-stu-id="1e1d9-110">Requirement</span></span> | <span data-ttu-id="1e1d9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1e1d9-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1d9-112">Версия</span><span class="sxs-lookup"><span data-stu-id="1e1d9-112">Version</span></span><br/> | <span data-ttu-id="1e1d9-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e1d9-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1e1d9-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e1d9-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1e1d9-115">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1e1d9-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1e1d9-116">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1e1d9-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e1d9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1e1d9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e1d9-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="1e1d9-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 
