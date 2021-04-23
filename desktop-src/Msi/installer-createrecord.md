---
description: Метод СоздатьЗапись объекта Installer возвращает новый объект Record с запрошенным числом полей.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Метод Installer. СоздатьЗапись
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652287"
---
# <a name="installercreaterecord-method"></a><span data-ttu-id="f719c-103">Метод Installer. СоздатьЗапись</span><span class="sxs-lookup"><span data-stu-id="f719c-103">Installer.CreateRecord method</span></span>

<span data-ttu-id="f719c-104">Метод **СоздатьЗапись** объекта [**Installer**](installer-object.md) возвращает новый объект [**Record**](record-object.md) с запрошенным числом полей.</span><span class="sxs-lookup"><span data-stu-id="f719c-104">The **CreateRecord** method of the [**Installer**](installer-object.md) object returns a new [**Record**](record-object.md) object with the requested number of fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="f719c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f719c-105">Syntax</span></span>


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a><span data-ttu-id="f719c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f719c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f719c-107">*count*</span><span class="sxs-lookup"><span data-stu-id="f719c-107">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="f719c-108">Требуемое число полей, которое может быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="f719c-108">Required number of fields, which may be 0.</span></span> <span data-ttu-id="f719c-109">Максимальное число полей в записи ограничено 65535.</span><span class="sxs-lookup"><span data-stu-id="f719c-109">The maximum number of fields in a record is limited to 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f719c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f719c-110">Return value</span></span>

<span data-ttu-id="f719c-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f719c-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f719c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f719c-112">Remarks</span></span>

<span data-ttu-id="f719c-113">Поле 0, а не одно из полей в *подсчете*, обычно используется для элементов, ориентированных на запись, таких как строки формата или Op-коды выполнения.</span><span class="sxs-lookup"><span data-stu-id="f719c-113">Field 0, not one of the fields in *count*, is normally used for record-oriented items such as format strings or execution op-codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f719c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f719c-114">Requirements</span></span>



| <span data-ttu-id="f719c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f719c-115">Requirement</span></span> | <span data-ttu-id="f719c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f719c-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f719c-117">Версия</span><span class="sxs-lookup"><span data-stu-id="f719c-117">Version</span></span><br/> | <span data-ttu-id="f719c-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f719c-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f719c-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f719c-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f719c-120">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="f719c-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f719c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f719c-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="f719c-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f719c-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f719c-123">IID</span><span class="sxs-lookup"><span data-stu-id="f719c-123">IID</span></span><br/>     | <span data-ttu-id="f719c-124">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f719c-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




