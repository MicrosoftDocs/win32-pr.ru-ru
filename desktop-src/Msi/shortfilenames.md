---
description: Установка свойства ШОРТФИЛЕНАМЕС приводит к тому, что короткие имена файлов используются для имен целевых файлов, а не длинных имен файлов. Он не влияет на имена файлов, которые установщик ищет в источнике.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: ШОРТФИЛЕНАМЕС, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652275"
---
# <a name="shortfilenames-property"></a><span data-ttu-id="7624c-104">ШОРТФИЛЕНАМЕС, свойство</span><span class="sxs-lookup"><span data-stu-id="7624c-104">SHORTFILENAMES property</span></span>

<span data-ttu-id="7624c-105">Установка свойства **шортфиленамес** приводит к тому, что короткие имена файлов используются для имен целевых файлов, а не длинных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="7624c-105">Setting the **SHORTFILENAMES** property causes short file names to be used for the names of target files, rather than long file names.</span></span> <span data-ttu-id="7624c-106">Он не влияет на имена файлов, которые установщик ищет в источнике.</span><span class="sxs-lookup"><span data-stu-id="7624c-106">It does not affect the file names the installer looks for at the source.</span></span>

## <a name="default-value"></a><span data-ttu-id="7624c-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7624c-107">Default Value</span></span>

<span data-ttu-id="7624c-108">Если свойство **шортфиленамес** не задано и целевой том поддерживает длинные имена, установщик использует длинные имена.</span><span class="sxs-lookup"><span data-stu-id="7624c-108">Long names are used by the installer if the **SHORTFILENAMES** property is not set and the target volume supports long names.</span></span> <span data-ttu-id="7624c-109">Короткие имена используются программой установки, если целевой том не поддерживает длинные имена.</span><span class="sxs-lookup"><span data-stu-id="7624c-109">Short names are used by the installer if the target volume does not support long names.</span></span>

## <a name="remarks"></a><span data-ttu-id="7624c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7624c-110">Remarks</span></span>

<span data-ttu-id="7624c-111">Если задано свойство **шортфиленамес** , установщик создает папки и устанавливает файлы с использованием коротких имен файлов из всех коротких \| длинных пар, перечисленных в таблице [файлов](file-table.md) или [таблице каталогов](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="7624c-111">When the **SHORTFILENAMES** property is set, the installer creates folders and installs files using short file names from any short\|long pairs listed in the [File table](file-table.md) or [Directory table](directory-table.md).</span></span>

<span data-ttu-id="7624c-112">Приложения могут использовать функцию [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) для получения короткого пути к указанному пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="7624c-112">Applications can use the [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) function to retrieve the short path form of a specified file path.</span></span>

## <a name="requirements"></a><span data-ttu-id="7624c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7624c-113">Requirements</span></span>



| <span data-ttu-id="7624c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7624c-114">Requirement</span></span> | <span data-ttu-id="7624c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7624c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7624c-116">Версия</span><span class="sxs-lookup"><span data-stu-id="7624c-116">Version</span></span><br/> | <span data-ttu-id="7624c-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7624c-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7624c-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7624c-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7624c-119">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7624c-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7624c-120">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7624c-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7624c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="7624c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7624c-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="7624c-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 
