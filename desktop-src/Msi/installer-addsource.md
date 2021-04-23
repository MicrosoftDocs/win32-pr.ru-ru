---
description: Метод Аддсаурце объекта Installer добавляет источник в список допустимых сетевых источников в списке.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Метод Installer. Аддсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651896"
---
# <a name="installeraddsource-method"></a><span data-ttu-id="f05fb-103">Метод Installer. Аддсаурце</span><span class="sxs-lookup"><span data-stu-id="f05fb-103">Installer.AddSource method</span></span>

<span data-ttu-id="f05fb-104">Метод **аддсаурце** объекта [**Installer**](installer-object.md) добавляет источник в список допустимых сетевых источников в списке.</span><span class="sxs-lookup"><span data-stu-id="f05fb-104">The **AddSource** method of the [**Installer**](installer-object.md) object adds a source to the list of valid network sources in the sourcelist.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f05fb-105">Syntax</span></span>


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a><span data-ttu-id="f05fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f05fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f05fb-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="f05fb-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="f05fb-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="f05fb-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="f05fb-109">*Пользователь*</span><span class="sxs-lookup"><span data-stu-id="f05fb-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="f05fb-110">Имя пользователя для установки на уровне пользователя; значение null или пустая строка для установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f05fb-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> <dt>

<span data-ttu-id="f05fb-111">*Источник*</span><span class="sxs-lookup"><span data-stu-id="f05fb-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="f05fb-112">Указатель на строку, указывающую источник.</span><span class="sxs-lookup"><span data-stu-id="f05fb-112">Pointer to the string specifying the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f05fb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f05fb-113">Return value</span></span>

<span data-ttu-id="f05fb-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f05fb-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f05fb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f05fb-115">Requirements</span></span>



| <span data-ttu-id="f05fb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f05fb-116">Requirement</span></span> | <span data-ttu-id="f05fb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f05fb-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f05fb-118">Версия</span><span class="sxs-lookup"><span data-stu-id="f05fb-118">Version</span></span><br/> | <span data-ttu-id="f05fb-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f05fb-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f05fb-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f05fb-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f05fb-121">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="f05fb-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f05fb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f05fb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="f05fb-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f05fb-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f05fb-124">IID</span><span class="sxs-lookup"><span data-stu-id="f05fb-124">IID</span></span><br/>     | <span data-ttu-id="f05fb-125">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f05fb-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="f05fb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f05fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05fb-127">**мсисаурцелистаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="f05fb-127">**MsiSourceListAddSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[<span data-ttu-id="f05fb-128">отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="f05fb-128">source resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




