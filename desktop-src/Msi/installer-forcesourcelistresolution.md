---
description: Метод Форцесаурцелистресолутион объекта Installer заставляет установщик Windows искать допустимый источник продукта в списке источников.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Метод Installer. Форцесаурцелистресолутион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651601"
---
# <a name="installerforcesourcelistresolution-method"></a><span data-ttu-id="830a3-103">Метод Installer. Форцесаурцелистресолутион</span><span class="sxs-lookup"><span data-stu-id="830a3-103">Installer.ForceSourceListResolution method</span></span>

<span data-ttu-id="830a3-104">Метод **форцесаурцелистресолутион** объекта [**Installer**](installer-object.md) заставляет установщик выполнять поиск действительного источника продукта в исходном списке, например, когда установщик выполняет установку или переустановку, или когда ему требуется путь для запуска набора компонентов из источника данных, если он необходим.</span><span class="sxs-lookup"><span data-stu-id="830a3-104">The **ForceSourceListResolution** method of the [**Installer**](installer-object.md) object forces the installer to search the source list for a valid product source the next time a source is needed, such as when the installer performs an installation or a reinstallation, or when it needs the path for a component set to run from source.</span></span>

## <a name="syntax"></a><span data-ttu-id="830a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="830a3-105">Syntax</span></span>


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="830a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="830a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="830a3-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="830a3-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="830a3-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="830a3-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="830a3-109">*Пользователь*</span><span class="sxs-lookup"><span data-stu-id="830a3-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="830a3-110">Имя пользователя для установки на уровне пользователя; значение null или пустая строка для установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="830a3-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="830a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="830a3-111">Return value</span></span>

<span data-ttu-id="830a3-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="830a3-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="830a3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="830a3-113">Requirements</span></span>



| <span data-ttu-id="830a3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="830a3-114">Requirement</span></span> | <span data-ttu-id="830a3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="830a3-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="830a3-116">Версия</span><span class="sxs-lookup"><span data-stu-id="830a3-116">Version</span></span><br/> | <span data-ttu-id="830a3-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="830a3-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="830a3-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="830a3-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="830a3-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="830a3-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="830a3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="830a3-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="830a3-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="830a3-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="830a3-122">IID</span><span class="sxs-lookup"><span data-stu-id="830a3-122">IID</span></span><br/>     | <span data-ttu-id="830a3-123">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="830a3-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="830a3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="830a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="830a3-125">**мсисаурцелистфорцересолутион**</span><span class="sxs-lookup"><span data-stu-id="830a3-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="830a3-126">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="830a3-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




