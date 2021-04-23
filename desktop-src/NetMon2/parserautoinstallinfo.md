---
description: Функция экспорта Парсераутоинсталлинфо определяет средство синтаксического анализа или средства синтаксического анализа, которые находятся в библиотеке DLL. Парсераутоинсталлинфо должен быть реализован во всех библиотеках DLL средства синтаксического анализа.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Функция обратного вызова Парсераутоинсталлинфо (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342742"
---
# <a name="parserautoinstallinfo-callback-function"></a><span data-ttu-id="c567f-104">Функция обратного вызова Парсераутоинсталлинфо</span><span class="sxs-lookup"><span data-stu-id="c567f-104">ParserAutoInstallInfo callback function</span></span>

<span data-ttu-id="c567f-105">Функция экспорта **парсераутоинсталлинфо** определяет средство синтаксического анализа или средства синтаксического анализа, которые находятся в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="c567f-105">The **ParserAutoInstallInfo** export function identifies the parser, or parsers that are located in a DLL.</span></span> <span data-ttu-id="c567f-106">**Парсераутоинсталлинфо** должен быть реализован во всех библиотеках DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c567f-106">**ParserAutoInstallInfo** should be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c567f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c567f-107">Syntax</span></span>


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a><span data-ttu-id="c567f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c567f-108">Parameters</span></span>

<span data-ttu-id="c567f-109">Эта функция обратного вызова не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c567f-109">This callback function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c567f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c567f-110">Return value</span></span>

<span data-ttu-id="c567f-111">Если функция выполнена успешно, возвращаемое значение является структурой [PF \_ парсердллинфо](pf-parserdllinfo.md) , описывающей ПАРСЕРЫ в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="c567f-111">If the function is successful, the return value is a [PF\_PARSERDLLINFO](pf-parserdllinfo.md) structure that describes the parsers in the DLL.</span></span>

<span data-ttu-id="c567f-112">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="c567f-112">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c567f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c567f-113">Remarks</span></span>

<span data-ttu-id="c567f-114">При первой загрузке сетевой монитор вызывает метод **парсераутоинсталлинфо** (если он существует) для автоматической установки каждого средства синтаксического анализа, а затем перечислите все библиотеки DLL средства синтаксического анализа в подкаталоге средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c567f-114">When Network Monitor loads for the first time, it calls **ParserAutoInstallInfo** (if it exists) to automatically install each parser, and then enumerate all the parser DLLs in the parser subdirectory.</span></span>

<span data-ttu-id="c567f-115">Сведения, возвращаемые в структуре **PF \_ парсердллинфо** , включают следующее:</span><span class="sxs-lookup"><span data-stu-id="c567f-115">The information returned in the **PF\_PARSERDLLINFO** structure includes the following:</span></span>

-   <span data-ttu-id="c567f-116">Количество синтаксических анализаторов в библиотеке DLL (обычно один).</span><span class="sxs-lookup"><span data-stu-id="c567f-116">The number of parsers in the DLL (typically one).</span></span>
-   <span data-ttu-id="c567f-117">Имя и краткое описание протокола, обнаруженного каждым синтаксическим анализатором.</span><span class="sxs-lookup"><span data-stu-id="c567f-117">The name and a brief description of the protocol that each parser detects.</span></span>
-   <span data-ttu-id="c567f-118">Необязательный файл справки для каждого протокола.</span><span class="sxs-lookup"><span data-stu-id="c567f-118">An optional Help file for each protocol.</span></span>
-   <span data-ttu-id="c567f-119">Протоколы, предшествующие каждому протоколу.</span><span class="sxs-lookup"><span data-stu-id="c567f-119">The protocols that precede each protocol.</span></span>
-   <span data-ttu-id="c567f-120">Протоколы, которые следуют каждому протоколу.</span><span class="sxs-lookup"><span data-stu-id="c567f-120">The protocols that follow each protocol.</span></span>

<span data-ttu-id="c567f-121">Каждая библиотека DLL анализатора должна содержать одно средство синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c567f-121">Each parser DLL should contain one parser.</span></span> <span data-ttu-id="c567f-122">Однако сетевой монитор позволяет создать библиотеку DLL, содержащую более одного средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c567f-122">However, Network Monitor allows you to create a DLL that contains more than one parser.</span></span> <span data-ttu-id="c567f-123">Например, tcpip.dll является сетевой монитор DLL с несколькими анализаторами.</span><span class="sxs-lookup"><span data-stu-id="c567f-123">For example, tcpip.dll is a Network Monitor DLL with more than one parser.</span></span>



| <span data-ttu-id="c567f-124">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="c567f-124">For information on</span></span>                                               | <span data-ttu-id="c567f-125">См.</span><span class="sxs-lookup"><span data-stu-id="c567f-125">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c567f-126">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="c567f-126">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="c567f-127">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="c567f-127">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="c567f-128">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c567f-128">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="c567f-129">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="c567f-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="c567f-130">Реализация **парсераутоинсталлинфо**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="c567f-130">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="c567f-131">Реализация Парсераутоинсталлинфо</span><span class="sxs-lookup"><span data-stu-id="c567f-131">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="c567f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="c567f-132">Requirements</span></span>



| <span data-ttu-id="c567f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="c567f-133">Requirement</span></span> | <span data-ttu-id="c567f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c567f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c567f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c567f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c567f-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c567f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c567f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c567f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c567f-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c567f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c567f-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c567f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c567f-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c567f-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c567f-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c567f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c567f-142">PF \_ парсердллинфо</span><span class="sxs-lookup"><span data-stu-id="c567f-142">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




