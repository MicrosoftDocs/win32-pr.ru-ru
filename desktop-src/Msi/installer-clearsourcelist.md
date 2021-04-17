---
description: Метод Клеарсаурцелист объекта Installer удаляет все сетевые источники из исходного списка.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Метод Installer. Клеарсаурцелист
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651810"
---
# <a name="installerclearsourcelist-method"></a><span data-ttu-id="0d833-103">Метод Installer. Клеарсаурцелист</span><span class="sxs-lookup"><span data-stu-id="0d833-103">Installer.ClearSourceList method</span></span>

<span data-ttu-id="0d833-104">Метод **клеарсаурцелист** объекта [**Installer**](installer-object.md) удаляет все сетевые источники из исходного списка.</span><span class="sxs-lookup"><span data-stu-id="0d833-104">The **ClearSourceList** method of the [**Installer**](installer-object.md) object removes all network sources from the source list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d833-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d833-105">Syntax</span></span>


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="0d833-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d833-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d833-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="0d833-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="0d833-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="0d833-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="0d833-109">*Пользователь*</span><span class="sxs-lookup"><span data-stu-id="0d833-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="0d833-110">Имя пользователя для установки на уровне пользователя; значение null или пустая строка для установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0d833-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d833-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d833-111">Return value</span></span>

<span data-ttu-id="0d833-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0d833-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d833-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0d833-113">Requirements</span></span>



| <span data-ttu-id="0d833-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0d833-114">Requirement</span></span> | <span data-ttu-id="0d833-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0d833-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d833-116">Версия</span><span class="sxs-lookup"><span data-stu-id="0d833-116">Version</span></span><br/> | <span data-ttu-id="0d833-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d833-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d833-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d833-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d833-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d833-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0d833-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0d833-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d833-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d833-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0d833-122">IID</span><span class="sxs-lookup"><span data-stu-id="0d833-122">IID</span></span><br/>     | <span data-ttu-id="0d833-123">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0d833-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0d833-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d833-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d833-125">**мсисаурцелистклеаралл**</span><span class="sxs-lookup"><span data-stu-id="0d833-125">**MsiSourceListClearAll**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[<span data-ttu-id="0d833-126">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="0d833-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




