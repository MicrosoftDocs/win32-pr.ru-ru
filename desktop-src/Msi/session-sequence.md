---
description: Метод Sequence объекта Session открывает запрос к указанной таблице, упорядочивая действия по числам в столбце последовательности.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652246"
---
# <a name="sessionsequence-method"></a><span data-ttu-id="886f1-103">Session. Sequence, метод</span><span class="sxs-lookup"><span data-stu-id="886f1-103">Session.Sequence method</span></span>

<span data-ttu-id="886f1-104">Метод **Sequence** объекта [**Session**](session-object.md) открывает запрос к указанной таблице, упорядочивая действия по числам в столбце последовательности.</span><span class="sxs-lookup"><span data-stu-id="886f1-104">The **Sequence** method of the [**Session**](session-object.md) object opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="886f1-105">Для каждой выбранной строки вызывается метод [**DoAction**](session-doaction.md) при условии, что любое предоставленное выражение условия не возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="886f1-105">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span> <span data-ttu-id="886f1-106">Возвращает Мсидоактионстатусенум перечисления, как описано в методе [**DoAction**](session-doaction.md) .</span><span class="sxs-lookup"><span data-stu-id="886f1-106">Returns an enumeration msiDoActionStatusEnum, as described in the [**DoAction**](session-doaction.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="886f1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="886f1-107">Syntax</span></span>


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a><span data-ttu-id="886f1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="886f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="886f1-109">*table*</span><span class="sxs-lookup"><span data-stu-id="886f1-109">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="886f1-110">Обязательное строковое имя таблицы, используемой для виртуализации.</span><span class="sxs-lookup"><span data-stu-id="886f1-110">Required string name of the table to use for sequencing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="886f1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="886f1-111">Return value</span></span>

<span data-ttu-id="886f1-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="886f1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="886f1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="886f1-113">Remarks</span></span>

<span data-ttu-id="886f1-114">Этот метод обычно вызывается внутренним действием верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="886f1-114">This method is normally called internally by top-level actions.</span></span>

<span data-ttu-id="886f1-115">Последовательность действий, содержащая действия, которые обновляют систему, такие как действия [инсталлфилес](installfiles-action.md) и [вритерегистривалуес](writeregistryvalues-action.md) , не может быть выполнена путем вызова метода **Sequence** .</span><span class="sxs-lookup"><span data-stu-id="886f1-115">An action sequence containing actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **Sequence** method.</span></span> <span data-ttu-id="886f1-116">Исключением из этого правила является то, что метод **Sequence** вызывается из настраиваемого действия, запланированного в [таблице инсталлексекутесекуенце](installexecutesequence-table.md) между [действиями](installfinalize-action.md) [инсталлинитиализе](installinitialize-action.md) и функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="886f1-116">The exception to this rule is if the **Sequence** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="886f1-117">Действия, которые не обновляют систему, например [аппсеарч](appsearch-action.md) или [костинитиализе](costinitialize-action.md), могут быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="886f1-117">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="886f1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="886f1-118">Requirements</span></span>



| <span data-ttu-id="886f1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="886f1-119">Requirement</span></span> | <span data-ttu-id="886f1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="886f1-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="886f1-121">Версия</span><span class="sxs-lookup"><span data-stu-id="886f1-121">Version</span></span><br/> | <span data-ttu-id="886f1-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="886f1-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="886f1-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="886f1-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="886f1-124">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="886f1-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="886f1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="886f1-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="886f1-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="886f1-127">IID</span><span class="sxs-lookup"><span data-stu-id="886f1-127">IID</span></span><br/>     | <span data-ttu-id="886f1-128">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="886f1-128">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




