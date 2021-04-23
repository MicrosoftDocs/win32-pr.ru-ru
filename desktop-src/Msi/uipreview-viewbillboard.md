---
description: Метод Виевбиллбоард объекта Уипревиев отображает созданное объявление, используя элемент управления ведущего приложения в отображаемом в данный момент диалоговом окне.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Уипревиев. Виевбиллбоард, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651878"
---
# <a name="uipreviewviewbillboard-method"></a><span data-ttu-id="58117-103">Уипревиев. Виевбиллбоард, метод</span><span class="sxs-lookup"><span data-stu-id="58117-103">UIPreview.ViewBillboard method</span></span>

<span data-ttu-id="58117-104">Метод **виевбиллбоард** объекта [**уипревиев**](uipreview-object.md) отображает созданное объявление, используя элемент управления ведущего приложения в отображаемом в данный момент диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="58117-104">The **ViewBillboard** method of the [**UIPreview**](uipreview-object.md) object displays an authored billboard using the host control in the currently displayed dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="58117-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58117-105">Syntax</span></span>


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a><span data-ttu-id="58117-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="58117-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58117-107">*control*</span><span class="sxs-lookup"><span data-stu-id="58117-107">*control*</span></span> 
</dt> <dd>

<span data-ttu-id="58117-108">Обязательное имя элемента управления, в котором размещается объявление, с учетом регистра, вместе с диалоговым окном и первичными ключами таблицы управляющей базы данных.</span><span class="sxs-lookup"><span data-stu-id="58117-108">Required name of the control hosting the billboard, case-sensitive, along with the dialog box, and the primary keys of the Control database table.</span></span>

</dd> <dt>

<span data-ttu-id="58117-109">*печат*</span><span class="sxs-lookup"><span data-stu-id="58117-109">*billboard*</span></span> 
</dt> <dd>

<span data-ttu-id="58117-110">Обязательное имя объявления, которое будет отображаться с использованием указанного элемента управления и текущего диалогового окна, и первичного ключа таблицы базы данных объявления.</span><span class="sxs-lookup"><span data-stu-id="58117-110">Required name of the billboard to display using the specified control and current dialog box, and the primary key of the Billboard database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58117-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58117-111">Return value</span></span>

<span data-ttu-id="58117-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="58117-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="58117-113">Требования</span><span class="sxs-lookup"><span data-stu-id="58117-113">Requirements</span></span>



| <span data-ttu-id="58117-114">Требование</span><span class="sxs-lookup"><span data-stu-id="58117-114">Requirement</span></span> | <span data-ttu-id="58117-115">Значение</span><span class="sxs-lookup"><span data-stu-id="58117-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58117-116">Версия</span><span class="sxs-lookup"><span data-stu-id="58117-116">Version</span></span><br/> | <span data-ttu-id="58117-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="58117-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="58117-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="58117-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="58117-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="58117-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="58117-120">DLL</span><span class="sxs-lookup"><span data-stu-id="58117-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="58117-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58117-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="58117-122">IID</span><span class="sxs-lookup"><span data-stu-id="58117-122">IID</span></span><br/>     | <span data-ttu-id="58117-123">IID \_ иуипревиев определяется как 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="58117-123">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




