---
description: Метод Мержеекс объекта Merge эквивалентен функции MERGE, за исключением того, что она принимает дополнительный аргумент.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Метод Merge. Мержеекс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675189"
---
# <a name="mergemergeex-method"></a><span data-ttu-id="695c7-103">Метод Merge. Мержеекс</span><span class="sxs-lookup"><span data-stu-id="695c7-103">Merge.MergeEx method</span></span>

<span data-ttu-id="695c7-104">Метод **мержеекс** объекта [**Merge**](merge-object.md) эквивалентен функции [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , за исключением того, что она принимает дополнительный аргумент.</span><span class="sxs-lookup"><span data-stu-id="695c7-104">The **MergeEx** method of the [**Merge**](merge-object.md) object is equivalent to the [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function, except that it takes an extra argument.</span></span> <span data-ttu-id="695c7-105">Аргумент *пконфигуратион* — это интерфейс, реализуемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="695c7-105">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="695c7-106">Аргумент может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="695c7-106">The argument may be null.</span></span> <span data-ttu-id="695c7-107">Наличие этого аргумента указывает, что клиент способен поддерживать функциональность конфигурации, но не несет клиенту предоставления данных конфигурации для конкретного настраиваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="695c7-107">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

<span data-ttu-id="695c7-108">Метод [**Merge**](merge-merge.md) выполняет слияние текущей базы данных и текущего модуля.</span><span class="sxs-lookup"><span data-stu-id="695c7-108">The [**Merge**](merge-merge.md) method executes a merge of the current database and current module.</span></span> <span data-ttu-id="695c7-109">Слияние присоединяет компоненты модуля к функции, определяемой *функцией*.</span><span class="sxs-lookup"><span data-stu-id="695c7-109">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="695c7-110">Корень дерева каталогов модуля перенаправляется в расположение, заданное параметром *редиректдир*.</span><span class="sxs-lookup"><span data-stu-id="695c7-110">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

## <a name="syntax"></a><span data-ttu-id="695c7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="695c7-111">Syntax</span></span>


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a><span data-ttu-id="695c7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="695c7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695c7-113">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="695c7-113">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="695c7-114">Имя компонента в базе данных.</span><span class="sxs-lookup"><span data-stu-id="695c7-114">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="695c7-115">*редиректдир*</span><span class="sxs-lookup"><span data-stu-id="695c7-115">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="695c7-116">Ключ записи в [таблице Directory](directory-table.md) базы данных.</span><span class="sxs-lookup"><span data-stu-id="695c7-116">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="695c7-117">Этот параметр может иметь значение null или быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="695c7-117">This parameter may be null or an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="695c7-118">*пконфигуратион*</span><span class="sxs-lookup"><span data-stu-id="695c7-118">*pConfiguration*</span></span> 
</dt> <dd>

<span data-ttu-id="695c7-119">Аргумент *пконфигуратион* — это интерфейс, реализуемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="695c7-119">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="695c7-120">Аргумент может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="695c7-120">The argument may be null.</span></span> <span data-ttu-id="695c7-121">Наличие этого аргумента указывает, что клиент способен поддерживать функциональность конфигурации, но не несет клиенту предоставления данных конфигурации для конкретного настраиваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="695c7-121">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="695c7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="695c7-122">Return value</span></span>

<span data-ttu-id="695c7-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="695c7-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="695c7-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="695c7-124">Remarks</span></span>

<span data-ttu-id="695c7-125">После завершения слияния компоненты модуля присоединяются к функции, определяемой *компонентом*.</span><span class="sxs-lookup"><span data-stu-id="695c7-125">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="695c7-126">Эта функция не создана и должна быть существующей функцией.</span><span class="sxs-lookup"><span data-stu-id="695c7-126">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="695c7-127">Модуль можно подключить к дополнительным функциям с помощью метода [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="695c7-127">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span>

<span data-ttu-id="695c7-128">Изменения, вносимые в базу данных, сохраняются только в том случае, если метод [**клоседатабасе**](merge-closedatabase.md) вызывается с параметром *бкоммит* , для которого задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="695c7-128">Changes made to the database are saved if and only if the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="695c7-129">Если возникают конфликты слияния, включая исключения, они помещаются в перечислитель ошибок для последующего извлечения, но не приводят к сбою слияния.</span><span class="sxs-lookup"><span data-stu-id="695c7-129">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="695c7-130">Ошибки могут быть получены с помощью свойства [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="695c7-130">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="695c7-131">Ошибки и информационные сообщения отправляются в текущий файл журнала.</span><span class="sxs-lookup"><span data-stu-id="695c7-131">Errors and informational messages are posted to the current log file.</span></span>

<span data-ttu-id="695c7-132">Если слияние завершается неудачей из-за неверной конфигурации модуля, функция [**мержеекс**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) возвращает \_ ошибку E.</span><span class="sxs-lookup"><span data-stu-id="695c7-132">When the merge fails because of an incorrect module configuration the [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function returns E\_FAIL.</span></span> <span data-ttu-id="695c7-133">Сюда входят следующие ошибки Мсмеррортипе: **мсмеррорбаднуллсубститутион**, **мсмеррорбадсубститутионтипе**, **мсмеррорбаднуллреспонсе**, **msmErrorMissingConfigItem** и **msmErrorDataRequestFailed**.</span><span class="sxs-lookup"><span data-stu-id="695c7-133">This includes these msmErrorType errors: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem**, and **msmErrorDataRequestFailed**.</span></span> <span data-ttu-id="695c7-134">Эти ошибки приводят к тому, что слияние останавливается сразу же после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="695c7-134">These errors cause the merge to stop immediately when the error is encountered.</span></span> <span data-ttu-id="695c7-135">Объект Error по-прежнему добавляется в перечислитель, когда **мержеекс** возвращает E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="695c7-135">The error object is still added to the enumerator when **MergeEx** returns E\_FAIL.</span></span> <span data-ttu-id="695c7-136">Дополнительные сведения об ошибках Мсмеррортипе см. в разделе [**\_ функция Get Type (объект Error)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span><span class="sxs-lookup"><span data-stu-id="695c7-136">For more information about msmErrorType errors, see [**get\_Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span></span> <span data-ttu-id="695c7-137">Все остальные ошибки приводят к тому, что **мержеекс** возвращает \_ значение false и вызовет продолжение слияния.</span><span class="sxs-lookup"><span data-stu-id="695c7-137">All other errors cause **MergeEx** to return S\_FALSE and cause the merge to continue.</span></span>

### <a name="c"></a><span data-ttu-id="695c7-138">C++</span><span class="sxs-lookup"><span data-stu-id="695c7-138">C++</span></span>

<span data-ttu-id="695c7-139">См. раздел Функция [**мержеекс**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .</span><span class="sxs-lookup"><span data-stu-id="695c7-139">See [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="695c7-140">Требования</span><span class="sxs-lookup"><span data-stu-id="695c7-140">Requirements</span></span>



| <span data-ttu-id="695c7-141">Требование</span><span class="sxs-lookup"><span data-stu-id="695c7-141">Requirement</span></span> | <span data-ttu-id="695c7-142">Значение</span><span class="sxs-lookup"><span data-stu-id="695c7-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="695c7-143">Версия</span><span class="sxs-lookup"><span data-stu-id="695c7-143">Version</span></span><br/> | <span data-ttu-id="695c7-144">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="695c7-144">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="695c7-145">Header</span><span class="sxs-lookup"><span data-stu-id="695c7-145">Header</span></span><br/>  | <dl> <span data-ttu-id="695c7-146"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="695c7-146"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="695c7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="695c7-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="695c7-148"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="695c7-148"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
