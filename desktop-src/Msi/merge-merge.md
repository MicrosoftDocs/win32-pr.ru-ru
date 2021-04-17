---
description: Метод Merge объекта MERGE выполняет слияние текущей базы данных и текущего модуля.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Метод Merge. Merge (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652175"
---
# <a name="mergemerge-method"></a><span data-ttu-id="f15e0-103">Merge. Merge, метод</span><span class="sxs-lookup"><span data-stu-id="f15e0-103">Merge.Merge method</span></span>

<span data-ttu-id="f15e0-104">Метод **Merge** объекта [**Merge**](merge-object.md) выполняет слияние текущей базы данных и текущего модуля.</span><span class="sxs-lookup"><span data-stu-id="f15e0-104">The **Merge** method of the [**Merge**](merge-object.md) object executes a merge of the current database and current module.</span></span> <span data-ttu-id="f15e0-105">Слияние присоединяет компоненты модуля к функции, определяемой *функцией*.</span><span class="sxs-lookup"><span data-stu-id="f15e0-105">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="f15e0-106">Корень дерева каталогов модуля перенаправляется в расположение, заданное параметром *редиректдир*.</span><span class="sxs-lookup"><span data-stu-id="f15e0-106">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

<span data-ttu-id="f15e0-107">Метод **Merge** может вызываться только один раз для слияния определенного сочетания файлов MSI и MSM.</span><span class="sxs-lookup"><span data-stu-id="f15e0-107">The **Merge** method can only be called once to merge a particular combination of .msi and .msm files.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f15e0-108">Syntax</span></span>


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a><span data-ttu-id="f15e0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f15e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15e0-110">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="f15e0-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="f15e0-111">Имя компонента в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f15e0-111">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="f15e0-112">*редиректдир*</span><span class="sxs-lookup"><span data-stu-id="f15e0-112">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="f15e0-113">Ключ записи в [таблице Directory](directory-table.md) базы данных.</span><span class="sxs-lookup"><span data-stu-id="f15e0-113">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="f15e0-114">Этот параметр может иметь значение null или быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="f15e0-114">This parameter may be null or an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15e0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f15e0-115">Return value</span></span>

<span data-ttu-id="f15e0-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f15e0-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15e0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f15e0-117">Remarks</span></span>

<span data-ttu-id="f15e0-118">После завершения слияния компоненты модуля присоединяются к функции, определяемой *компонентом*.</span><span class="sxs-lookup"><span data-stu-id="f15e0-118">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="f15e0-119">Эта функция не создана и должна быть существующей функцией.</span><span class="sxs-lookup"><span data-stu-id="f15e0-119">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="f15e0-120">Обратите внимание, что метод **Merge** получает все ссылки на функции в модуле и замещает ссылку на компонент для всех вхождений идентификатора GUID NULL в базе данных модуля.</span><span class="sxs-lookup"><span data-stu-id="f15e0-120">Note that the **Merge** method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database.</span></span> <span data-ttu-id="f15e0-121">Дополнительные сведения см. [в разделе ссылки на функции в модулях слияния](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="f15e0-121">For more information, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>

<span data-ttu-id="f15e0-122">Модуль можно подключить к дополнительным функциям с помощью метода [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="f15e0-122">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span> <span data-ttu-id="f15e0-123">Обратите внимание, что при вызове метода **Connect** создаются только связи компонентов компонента.</span><span class="sxs-lookup"><span data-stu-id="f15e0-123">Note that calling the **Connect** method only creates feature-component associations.</span></span> <span data-ttu-id="f15e0-124">Строки, которые уже были объединены в базу данных, не изменяются.</span><span class="sxs-lookup"><span data-stu-id="f15e0-124">It does not modify the rows that have already been merged in to the database.</span></span>

<span data-ttu-id="f15e0-125">Изменения, вносимые в базу данных, сохраняются только в том случае, если метод [**клоседатабасе**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) вызывается с параметром *бкоммит* , для которого задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f15e0-125">Changes made to the database are saved if and only if the [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="f15e0-126">Если возникают конфликты слияния, включая исключения, они помещаются в перечислитель ошибок для последующего извлечения, но не приводят к сбою слияния.</span><span class="sxs-lookup"><span data-stu-id="f15e0-126">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="f15e0-127">Ошибки могут быть получены с помощью свойства [**Errors**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="f15e0-127">Errors may be retrieved through the [**Errors**](error-object.md) property.</span></span> <span data-ttu-id="f15e0-128">Ошибки и информационные сообщения отправляются в текущий файл журнала.</span><span class="sxs-lookup"><span data-stu-id="f15e0-128">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="f15e0-129">C++</span><span class="sxs-lookup"><span data-stu-id="f15e0-129">C++</span></span>

<span data-ttu-id="f15e0-130">См. раздел Функция [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) .</span><span class="sxs-lookup"><span data-stu-id="f15e0-130">See [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f15e0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f15e0-131">Requirements</span></span>



| <span data-ttu-id="f15e0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f15e0-132">Requirement</span></span> | <span data-ttu-id="f15e0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f15e0-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f15e0-134">Версия</span><span class="sxs-lookup"><span data-stu-id="f15e0-134">Version</span></span><br/> | <span data-ttu-id="f15e0-135">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f15e0-135">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="f15e0-136">Header</span><span class="sxs-lookup"><span data-stu-id="f15e0-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f15e0-137"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15e0-137"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="f15e0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f15e0-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="f15e0-139"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f15e0-139"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
