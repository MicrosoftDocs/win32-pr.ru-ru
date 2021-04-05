---
title: атрибут notify_flag
description: Атрибут \ notify \_ флаг \ предоставляет уведомление, определяющее, вызывается ли Серверная подпрограммы.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag атрибута MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068826"
---
# <a name="notify_flag-attribute"></a><span data-ttu-id="4db31-104">\_атрибут флага notify</span><span class="sxs-lookup"><span data-stu-id="4db31-104">notify\_flag attribute</span></span>

<span data-ttu-id="4db31-105">Атрибут **\[ \_ флага \] Notify** предоставляет уведомление, определяющее, вызывается ли Серверная подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="4db31-105">The **\[notify\_flag\]** attribute provides notification identifying whether a server routine is called.</span></span>

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="4db31-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4db31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db31-107">*имя процедуры*</span><span class="sxs-lookup"><span data-stu-id="4db31-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4db31-108">Имя удаленной процедуры, с которой \_ связана процедура уведомления об отметке.</span><span class="sxs-lookup"><span data-stu-id="4db31-108">Name of the remote procedure with which the notify\_flag procedure is associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4db31-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4db31-109">Remarks</span></span>

<span data-ttu-id="4db31-110">Атрибут **\[ \_ флага \] Notify** аналогичен применению к атрибуту **\[ Notify \]** .</span><span class="sxs-lookup"><span data-stu-id="4db31-110">The **\[notify\_flag\]** attribute is similar in usage to the **\[notify\]** attribute.</span></span>

<span data-ttu-id="4db31-111">Имя процедуры **\[ уведомления \_ флаг \]** — это имя удаленной процедуры с суффиксом **\_ Notify \_**.</span><span class="sxs-lookup"><span data-stu-id="4db31-111">The **\[notify\_flag\]** procedure name is the name of the remote procedure suffixed by **\_notify\_flag**.</span></span> <span data-ttu-id="4db31-112">Процедура **\_ \_ флага уведомления** не требует никаких параметров и не возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="4db31-112">The **\_notify\_flag** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="4db31-113">Прототип этой процедуры также создается в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="4db31-113">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="4db31-114">Например, если IDL-файл содержит следующее:</span><span class="sxs-lookup"><span data-stu-id="4db31-114">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="4db31-115">Укажите следующие сведения в ACF для MIDL, чтобы создать вызов **\_ \_ флага уведомления** :</span><span class="sxs-lookup"><span data-stu-id="4db31-115">Specify the following in the ACF for MIDL to generate the **\_notify\_flag** call:</span></span>

``` syntax
[notify_flag] MyProcedure();
```

<span data-ttu-id="4db31-116">Компилятор MIDL создаст код заглушки сервера, который содержит следующий вызов процедуры **\_ уведомления о \_ флаге** :</span><span class="sxs-lookup"><span data-stu-id="4db31-116">The MIDL compiler will generate server stub code which contains the following call to the **\_notify\_flag** procedure:</span></span>

``` syntax
MyProcedure_notify_flag();
```

<span data-ttu-id="4db31-117">Файл заголовка будет содержать прототип:</span><span class="sxs-lookup"><span data-stu-id="4db31-117">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

<span data-ttu-id="4db31-118">**\_ MIDL \_ Нотифифлаг** имеет **значение true** , если вызывается Серверная подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="4db31-118">**\_MIDL\_NotifyFlag** is **TRUE** if the server routine is called.</span></span>

## <a name="examples"></a><span data-ttu-id="4db31-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="4db31-119">Examples</span></span>

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="4db31-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4db31-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db31-121">**явлении**</span><span class="sxs-lookup"><span data-stu-id="4db31-121">**notify**</span></span>](notify.md)
</dt> </dl>

 

 




