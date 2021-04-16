---
description: Свойство Верифидискспаце доступно только для чтения.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Свойство Session. Верифидискспаце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679936"
---
# <a name="sessionverifydiskspace-property"></a><span data-ttu-id="718e6-103">Свойство Session. Верифидискспаце</span><span class="sxs-lookup"><span data-stu-id="718e6-103">Session.VerifyDiskSpace property</span></span>

<span data-ttu-id="718e6-104">Свойство **верифидискспаце** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="718e6-104">The **VerifyDiskSpace** property is a read-only property.</span></span> <span data-ttu-id="718e6-105">Он возвращает значение true, если существует достаточно места на диске, и значение false, если диск заполнен.</span><span class="sxs-lookup"><span data-stu-id="718e6-105">It returns true if enough disk space exists and false if the disk is full.</span></span> <span data-ttu-id="718e6-106">Поскольку это свойство использует сведения, собранные действиями по затратам, **верифидискспаце** следует вызывать только после действия [костинитиализе](costinitialize-action.md), [филекост Action](filecost-action.md)и [костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="718e6-106">Because this property uses information gathered by the costing actions, **VerifyDiskSpace** should only be called after the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="718e6-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="718e6-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="718e6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="718e6-108">Syntax</span></span>


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a><span data-ttu-id="718e6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="718e6-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="718e6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="718e6-110">Requirements</span></span>



| <span data-ttu-id="718e6-111">Требование</span><span class="sxs-lookup"><span data-stu-id="718e6-111">Requirement</span></span> | <span data-ttu-id="718e6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="718e6-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="718e6-113">Версия</span><span class="sxs-lookup"><span data-stu-id="718e6-113">Version</span></span><br/> | <span data-ttu-id="718e6-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="718e6-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="718e6-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="718e6-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="718e6-116">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="718e6-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="718e6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="718e6-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="718e6-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="718e6-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="718e6-119">IID</span><span class="sxs-lookup"><span data-stu-id="718e6-119">IID</span></span><br/>     | <span data-ttu-id="718e6-120">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="718e6-120">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




