---
description: Метод Евалуатекондитион объекта Session вычисляет логическое выражение, содержащее символы и значения. Этот метод использует функцию Мсиевалуатекондитион.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session. Евалуатекондитион, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675722"
---
# <a name="sessionevaluatecondition-method"></a><span data-ttu-id="e4d3c-104">Session. Евалуатекондитион, метод</span><span class="sxs-lookup"><span data-stu-id="e4d3c-104">Session.EvaluateCondition method</span></span>

<span data-ttu-id="e4d3c-105">Метод **евалуатекондитион** объекта [**Session**](session-object.md) вычисляет логическое выражение, содержащее символы и значения.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-105">The **EvaluateCondition** method of the [**Session**](session-object.md) object evaluates a logical expression that contains symbols and values.</span></span> <span data-ttu-id="e4d3c-106">Этот метод использует функцию [**мсиевалуатекондитион**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="e4d3c-106">This method uses the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d3c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4d3c-107">Syntax</span></span>


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a><span data-ttu-id="e4d3c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4d3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d3c-109">*выполняет*</span><span class="sxs-lookup"><span data-stu-id="e4d3c-109">*condition*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d3c-110">Обязательная строка, содержащая логическое выражение.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-110">Required string that contains the logical expression.</span></span> <span data-ttu-id="e4d3c-111">Дополнительные сведения см. в разделе [Синтаксис условных инструкций](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e4d3c-111">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d3c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4d3c-112">Return value</span></span>

<span data-ttu-id="e4d3c-113">Этот метод возвращает целое число, указывающее на вычисление условия.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-113">This method returns an integer that indicates the evaluation of the condition.</span></span>



| <span data-ttu-id="e4d3c-114">Константа</span><span class="sxs-lookup"><span data-stu-id="e4d3c-114">Constant</span></span>                  | <span data-ttu-id="e4d3c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e4d3c-115">Value</span></span> | <span data-ttu-id="e4d3c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e4d3c-116">Description</span></span>                               |
|---------------------------|-------|-------------------------------------------|
| <span data-ttu-id="e4d3c-117">мсиевалуатекондитионфалсе</span><span class="sxs-lookup"><span data-stu-id="e4d3c-117">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="e4d3c-118">0</span><span class="sxs-lookup"><span data-stu-id="e4d3c-118">0</span></span>     | <span data-ttu-id="e4d3c-119">Условие принимает значение false.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-119">The condition evaluates to false.</span></span>         |
| <span data-ttu-id="e4d3c-120">мсиевалуатекондитионтруе</span><span class="sxs-lookup"><span data-stu-id="e4d3c-120">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="e4d3c-121">1</span><span class="sxs-lookup"><span data-stu-id="e4d3c-121">1</span></span>     | <span data-ttu-id="e4d3c-122">Условие принимает значение true.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-122">The condition evaluates to true.</span></span>          |
| <span data-ttu-id="e4d3c-123">мсиевалуатекондитионноне</span><span class="sxs-lookup"><span data-stu-id="e4d3c-123">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="e4d3c-124">2</span><span class="sxs-lookup"><span data-stu-id="e4d3c-124">2</span></span>     | <span data-ttu-id="e4d3c-125">Условное выражение не указано.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-125">A conditional expression is not provided.</span></span> |
| <span data-ttu-id="e4d3c-126">мсиевалуатекондитионеррор</span><span class="sxs-lookup"><span data-stu-id="e4d3c-126">msiEvaluateConditionError</span></span> | <span data-ttu-id="e4d3c-127">3</span><span class="sxs-lookup"><span data-stu-id="e4d3c-127">3</span></span>     | <span data-ttu-id="e4d3c-128">Условие содержит синтаксическую ошибку.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-128">The condition contains a syntax error.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="e4d3c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4d3c-129">Remarks</span></span>

<span data-ttu-id="e4d3c-130">Условные выражения можно использовать для сравнения состояний компонентов и компонентов.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-130">Conditional expressions can be used to compare feature and component states.</span></span> <span data-ttu-id="e4d3c-131">В следующей таблице показаны компоненты и состояния компонентов, используемые методом Евалуатекондитион.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-131">The following table shows the feature and component states that the EvaluateCondition method uses.</span></span>



| <span data-ttu-id="e4d3c-132">Состояние</span><span class="sxs-lookup"><span data-stu-id="e4d3c-132">State</span></span>                 | <span data-ttu-id="e4d3c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e4d3c-133">Value</span></span> | <span data-ttu-id="e4d3c-134">Описание</span><span class="sxs-lookup"><span data-stu-id="e4d3c-134">Description</span></span>                                              |
|-----------------------|-------|----------------------------------------------------------|
| <span data-ttu-id="e4d3c-135">NULL</span><span class="sxs-lookup"><span data-stu-id="e4d3c-135">Null</span></span>                  | <span data-ttu-id="e4d3c-136">NULL</span><span class="sxs-lookup"><span data-stu-id="e4d3c-136">Null</span></span>  | <span data-ttu-id="e4d3c-137">Для компонента или компонента не предпринято никаких действий.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-137">No action taken on feature or component.</span></span>                 |
| <span data-ttu-id="e4d3c-138">мсиинсталлстатеабсент</span><span class="sxs-lookup"><span data-stu-id="e4d3c-138">msiInstallStateAbsent</span></span> | <span data-ttu-id="e4d3c-139">2</span><span class="sxs-lookup"><span data-stu-id="e4d3c-139">2</span></span>     | <span data-ttu-id="e4d3c-140">Отсутствует компонент или компонент.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-140">Feature or component is not present.</span></span>                     |
| <span data-ttu-id="e4d3c-141">мсиинсталлстателокал</span><span class="sxs-lookup"><span data-stu-id="e4d3c-141">msiInstallStateLocal</span></span>  | <span data-ttu-id="e4d3c-142">3</span><span class="sxs-lookup"><span data-stu-id="e4d3c-142">3</span></span>     | <span data-ttu-id="e4d3c-143">Компонент или компонент установлен на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-143">Feature or component is installed on the local computer.</span></span> |
| <span data-ttu-id="e4d3c-144">мсиинсталлстатесаурце</span><span class="sxs-lookup"><span data-stu-id="e4d3c-144">msiInstallStateSource</span></span> | <span data-ttu-id="e4d3c-145">4</span><span class="sxs-lookup"><span data-stu-id="e4d3c-145">4</span></span>     | <span data-ttu-id="e4d3c-146">Компонент или компонент установлен для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-146">Feature or component is installed to run from source.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="e4d3c-147">Состояния не задаются, пока не будет вызван метод [**сетинсталллевел**](session-setinstalllevel.md) , либо напрямую, либо с помощью [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e4d3c-147">The states are not set until the [**SetInstallLevel**](session-setinstalllevel.md) method is called, either directly or by the [CostFinalize Action](costfinalize-action.md).</span></span> <span data-ttu-id="e4d3c-148">Поэтому проверка состояния полезна только в условных выражениях в таблице последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-148">Therefore, state checking is only useful in conditional expression in an action sequence table.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e4d3c-149">Требования</span><span class="sxs-lookup"><span data-stu-id="e4d3c-149">Requirements</span></span>



| <span data-ttu-id="e4d3c-150">Требование</span><span class="sxs-lookup"><span data-stu-id="e4d3c-150">Requirement</span></span> | <span data-ttu-id="e4d3c-151">Значение</span><span class="sxs-lookup"><span data-stu-id="e4d3c-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d3c-152">Версия</span><span class="sxs-lookup"><span data-stu-id="e4d3c-152">Version</span></span><br/> | <span data-ttu-id="e4d3c-153">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-153">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e4d3c-154">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-154">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e4d3c-155">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d3c-155">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e4d3c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e4d3c-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="e4d3c-157"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4d3c-157"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e4d3c-158">IID</span><span class="sxs-lookup"><span data-stu-id="e4d3c-158">IID</span></span><br/>     | <span data-ttu-id="e4d3c-159">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e4d3c-159">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="e4d3c-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4d3c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d3c-161">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="e4d3c-161">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 




