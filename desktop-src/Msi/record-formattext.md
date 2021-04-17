---
description: Метод Форматтекст объекта Record форматирует поля в соответствии с шаблоном в поле 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Метод Record. Форматтекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652106"
---
# <a name="recordformattext-method"></a><span data-ttu-id="a41a5-103">Метод Record. Форматтекст</span><span class="sxs-lookup"><span data-stu-id="a41a5-103">Record.FormatText method</span></span>

<span data-ttu-id="a41a5-104">Метод **форматтекст** объекта [**Record**](record-object.md) форматирует поля в соответствии с шаблоном в поле 0.</span><span class="sxs-lookup"><span data-stu-id="a41a5-104">The **FormatText** method of the [**Record**](record-object.md) object formats fields according to the template in field 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="a41a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a41a5-105">Syntax</span></span>


```JScript
Record.FormatText()
```



## <a name="parameters"></a><span data-ttu-id="a41a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a41a5-106">Parameters</span></span>

<span data-ttu-id="a41a5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a41a5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a41a5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a41a5-108">Return value</span></span>

<span data-ttu-id="a41a5-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a41a5-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a41a5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a41a5-110">Remarks</span></span>

<span data-ttu-id="a41a5-111">Метод **форматтекст** соответствует функциональным возможностям функции [**Мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) , если **мсиформатрекорд** был передан нулевой обработчик установщика в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="a41a5-111">The **FormatText** method follows the functionality of the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function if **MsiFormatRecord** was passed a null installer handle as its first parameter.</span></span> <span data-ttu-id="a41a5-112">В результате обрабатываются только параметры поля записи, а свойства для подстановки недоступны.</span><span class="sxs-lookup"><span data-stu-id="a41a5-112">As a result, only the record field parameters are processed and properties are not available for substitution.</span></span>

<span data-ttu-id="a41a5-113">Например, строка «форматирование этого поля: \[ 1 \] , форматирование этого свойства: \[ свойство \] » разрешается в «форматировать это поле: значение из поля 1», отформатировать это свойство: \[ свойство \] .</span><span class="sxs-lookup"><span data-stu-id="a41a5-113">For example, a string such as "format this field: \[1\], format this property: \[property\]" is resolved to "format this field: value from field 1, format this property: \[property\]."</span></span>

<span data-ttu-id="a41a5-114">Параметры, которые необходимо [отформатировать](formatted.md) , заключаются в квадратные скобки \[ . \] ..</span><span class="sxs-lookup"><span data-stu-id="a41a5-114">Parameters that are to be [formatted](formatted.md) are enclosed in square brackets \[...\].</span></span> <span data-ttu-id="a41a5-115">Можно выполнить итерацию квадратных скобок, так как подстановки разрешаются из внутренней области.</span><span class="sxs-lookup"><span data-stu-id="a41a5-115">The square brackets can be iterated because the substitutions are resolved from the inside out.</span></span>

<span data-ttu-id="a41a5-116">Если часть строки заключена в фигурные скобки {} и не содержит квадратных скобок, она остается без изменений, включая фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="a41a5-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="a41a5-117">Примечание. в случае [отложенного выполнения настраиваемых действий](deferred-execution-custom-actions.md) **форматтекст** поддерживает только ограниченный набор свойств: свойства CustomActionData и ProductCode.</span><span class="sxs-lookup"><span data-stu-id="a41a5-117">Note in the case of [deferred execution custom actions](deferred-execution-custom-actions.md), **FormatText** only supports a limited set of properties: the CustomActionData and ProductCode properties.</span></span> <span data-ttu-id="a41a5-118">Дополнительные сведения см. в разделе [Получение контекстных сведений для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a41a5-118">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a41a5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a41a5-119">Requirements</span></span>



| <span data-ttu-id="a41a5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a41a5-120">Requirement</span></span> | <span data-ttu-id="a41a5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a41a5-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a41a5-122">Версия</span><span class="sxs-lookup"><span data-stu-id="a41a5-122">Version</span></span><br/> | <span data-ttu-id="a41a5-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a41a5-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a41a5-124">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a41a5-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a41a5-125">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="a41a5-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a41a5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a41a5-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a41a5-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a41a5-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a41a5-128">IID</span><span class="sxs-lookup"><span data-stu-id="a41a5-128">IID</span></span><br/>     | <span data-ttu-id="a41a5-129">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a41a5-129">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="a41a5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a41a5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41a5-131">**мсиформатрекорд**</span><span class="sxs-lookup"><span data-stu-id="a41a5-131">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[<span data-ttu-id="a41a5-132">Формате</span><span class="sxs-lookup"><span data-stu-id="a41a5-132">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="a41a5-133">Типы данных столбцов</span><span class="sxs-lookup"><span data-stu-id="a41a5-133">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




