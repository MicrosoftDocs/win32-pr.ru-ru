---
description: Свойство SummaryInformation объекта Installer возвращает объект Суммаринфо, который может использоваться для проверки, обновления и добавления свойств в поток сводных данных пакета или преобразования.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Свойство Installer. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651658"
---
# <a name="installersummaryinformation-property"></a><span data-ttu-id="cddb4-103">Свойство Installer. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="cddb4-103">Installer.SummaryInformation property</span></span>

<span data-ttu-id="cddb4-104">Свойство **SummaryInformation** объекта [**Installer**](installer-object.md) возвращает объект [**суммаринфо**](summaryinfo-object.md) , который может использоваться для проверки, обновления и добавления свойств в поток сводных данных пакета или преобразования.</span><span class="sxs-lookup"><span data-stu-id="cddb4-104">The **SummaryInformation** property of the [**Installer**](installer-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream of a package or transform.</span></span>

<span data-ttu-id="cddb4-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cddb4-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cddb4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cddb4-106">Syntax</span></span>


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="cddb4-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cddb4-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="cddb4-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cddb4-108">Remarks</span></span>

<span data-ttu-id="cddb4-109">Если для открытия существующего потока сводных данных используется значение *макспропертиес* больше 0, то перед закрытием объекта необходимо вызвать метод [**Persist**](summaryinfo-persist.md) .</span><span class="sxs-lookup"><span data-stu-id="cddb4-109">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="cddb4-110">В противном случае существующие данные о потоке будут утеряны.</span><span class="sxs-lookup"><span data-stu-id="cddb4-110">Failing to do this loses the existing stream information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cddb4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="cddb4-111">Requirements</span></span>



| <span data-ttu-id="cddb4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="cddb4-112">Requirement</span></span> | <span data-ttu-id="cddb4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cddb4-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cddb4-114">Версия</span><span class="sxs-lookup"><span data-stu-id="cddb4-114">Version</span></span><br/> | <span data-ttu-id="cddb4-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cddb4-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cddb4-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cddb4-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cddb4-117">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="cddb4-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cddb4-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cddb4-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="cddb4-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cddb4-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cddb4-120">IID</span><span class="sxs-lookup"><span data-stu-id="cddb4-120">IID</span></span><br/>     | <span data-ttu-id="cddb4-121">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cddb4-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




