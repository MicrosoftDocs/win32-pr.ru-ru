---
title: уведомление атрибута
description: Атрибут \ notify \ предписывает компилятору MIDL создать вызов процедуры \ notify \ на стороне сервера приложения.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- уведомить атрибут MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532597"
---
# <a name="notify-attribute"></a><span data-ttu-id="53dae-104">уведомление атрибута</span><span class="sxs-lookup"><span data-stu-id="53dae-104">notify attribute</span></span>

<span data-ttu-id="53dae-105">Атрибут **\[ Notify \]** предписывает компилятору MIDL создать вызов процедуры **\[ Notify \]** на стороне сервера приложения.</span><span class="sxs-lookup"><span data-stu-id="53dae-105">The **\[notify\]** attribute instructs the MIDL compiler to generate a call to a **\[notify\]** procedure on the server side of the application.</span></span>

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="53dae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53dae-107">*имя процедуры*</span><span class="sxs-lookup"><span data-stu-id="53dae-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="53dae-108">Имя удаленной процедуры, с которой будет связана процедура notify.</span><span class="sxs-lookup"><span data-stu-id="53dae-108">The name of the remote procedure with which the notify procedure will be associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53dae-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53dae-109">Remarks</span></span>

<span data-ttu-id="53dae-110">Процедура **\[ Notify \]** , вызываемая как результат атрибута **\[ Notify \]** , связана с определенной удаленной процедурой на сервере.</span><span class="sxs-lookup"><span data-stu-id="53dae-110">The **\[notify\]** procedure called as a result of the **\[notify\]** attribute is associated with a particular remote procedure on the server.</span></span> <span data-ttu-id="53dae-111">Он аналогичен функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="53dae-111">It is similar in concept to a callback function.</span></span> <span data-ttu-id="53dae-112">Заглушка вызывает процедуру **\[ Notify \]** после того, как все выходные аргументы удаленной процедуры, с которой она связана, были упакованы, а память, связанная с параметрами, освобождается.</span><span class="sxs-lookup"><span data-stu-id="53dae-112">The stub calls the **\[notify\]** procedure after all the output arguments of the remote procedure with which it is associated have been marshaled and any memory associated with the parameters is freed.</span></span> <span data-ttu-id="53dae-113">Подпрограммы **\[ Notify \]** вызываются в случае сбоя вызова до выполнения серверной программы.</span><span class="sxs-lookup"><span data-stu-id="53dae-113">The **\[notify\]** routine is called if a call fails before the server routine executes.</span></span> <span data-ttu-id="53dae-114">Например, если во время распаковки сервера происходит сбой из-за получения недопустимых данных от клиента, \[ \] вызывается подпрограммы notify.</span><span class="sxs-lookup"><span data-stu-id="53dae-114">For example, if a server fails during unmarshaling due to receipt of bad data from the client, the \[notify\] routine is called.</span></span>

<span data-ttu-id="53dae-115">Атрибут **\[ Notify \]** полезен для разработки приложений, получающих ресурсы в удаленных процедурах.</span><span class="sxs-lookup"><span data-stu-id="53dae-115">The **\[notify\]** attribute is useful to develop applications acquiring resources in remote procedures.</span></span> <span data-ttu-id="53dae-116">Затем эти ресурсы освобождаются в процедуре **\[ Notify \]** после полного маршалирования выходных параметров удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="53dae-116">These resources are then freed in the **\[notify\]** procedure after the output parameters of the remote procedure are fully marshaled.</span></span>

<span data-ttu-id="53dae-117">Имя процедуры **\[ Notify \]** — это имя удаленной процедуры с суффиксом **\_ Notify**.</span><span class="sxs-lookup"><span data-stu-id="53dae-117">The **\[notify\]** procedure name is the name of the remote procedure suffixed by **\_notify**.</span></span> <span data-ttu-id="53dae-118">Процедура **\_ Notify** не требует каких-либо параметров и не возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="53dae-118">The **\_notify** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="53dae-119">Прототип этой процедуры также создается в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="53dae-119">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="53dae-120">Например, если IDL-файл содержит следующее:</span><span class="sxs-lookup"><span data-stu-id="53dae-120">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="53dae-121">Укажите следующие сведения в ACF для MIDL, чтобы создать вызов **\_ Notify** :</span><span class="sxs-lookup"><span data-stu-id="53dae-121">Specify the following in the ACF for MIDL to generate the **\_notify** call:</span></span>

``` syntax
[notify] MyProcedure();
```

<span data-ttu-id="53dae-122">Компилятор MIDL создаст код заглушки сервера, который содержит следующий вызов процедуры **\_ Notify** :</span><span class="sxs-lookup"><span data-stu-id="53dae-122">The MIDL compiler will generate server stub code which contains the following call to the **\_notify** procedure:</span></span>

``` syntax
MyProcedure_notify();
```

<span data-ttu-id="53dae-123">Файл заголовка будет содержать прототип:</span><span class="sxs-lookup"><span data-stu-id="53dae-123">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a><span data-ttu-id="53dae-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="53dae-124">Examples</span></span>

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="53dae-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53dae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53dae-126">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="53dae-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> </dl>

 

 




