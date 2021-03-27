---
title: " Директивы ifdef и ifndef"
description: Директивы препроцессора, которые определяют, определена ли конкретная константа препроцессора или макрос.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- Директивы ifdef и ifndef HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069002"
---
# <a name="ifdef-and-ifndef-directives"></a><span data-ttu-id="0cbfd-104">\#\#директивы ifdef и ifndef</span><span class="sxs-lookup"><span data-stu-id="0cbfd-104">\#ifdef and \#ifndef Directives</span></span>

<span data-ttu-id="0cbfd-105">Директивы препроцессора, которые определяют, определена ли конкретная константа препроцессора или макрос.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-105">Preprocessor directives that determine whether a specific preprocessor constant or macro is defined.</span></span>



| <span data-ttu-id="0cbfd-106">\#*идентификатор* ifdef...</span><span class="sxs-lookup"><span data-stu-id="0cbfd-106">\#ifdef *identifier* ...</span></span>  |
|---------------------------|
| <span data-ttu-id="0cbfd-107">\#endif</span><span class="sxs-lookup"><span data-stu-id="0cbfd-107">\#endif</span></span>                   |
| <span data-ttu-id="0cbfd-108">\#*идентификатор* ifndef...</span><span class="sxs-lookup"><span data-stu-id="0cbfd-108">\#ifndef *identifier* ...</span></span> |
| <span data-ttu-id="0cbfd-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="0cbfd-109">\#endif</span></span>                   |



 

## <a name="parameters"></a><span data-ttu-id="0cbfd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cbfd-110">Parameters</span></span>



| <span data-ttu-id="0cbfd-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="0cbfd-111">Item</span></span>                                                                              | <span data-ttu-id="0cbfd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0cbfd-112">Description</span></span>                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="0cbfd-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*Идентификатор*</span><span class="sxs-lookup"><span data-stu-id="0cbfd-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="0cbfd-114">Идентификатор проверяемой константы или макроса.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-114">Identifier of the constant or macro to check.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0cbfd-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0cbfd-115">Remarks</span></span>

<span data-ttu-id="0cbfd-116">\#Директивы ifdef и ifndef можно использовать \# в любом месте, где можно использовать, [ \# Если](dx-graphics-hlsl-appendix-pre-if.md) может использоваться.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-116">You can use the \#ifdef and \#ifndef directives anywhere that the [\#if](dx-graphics-hlsl-appendix-pre-if.md) can be used.</span></span> <span data-ttu-id="0cbfd-117">\#Инструкция ifdef эквивалентна директиве.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-117">The \#ifdef statement is equivalent to ) directive.</span></span> <span data-ttu-id="0cbfd-118">Эти директивы проверяют только на наличие или отсутствие идентификаторов, определенных с помощью директивы [ \# define](dx-graphics-hlsl-appendix-pre-define.md) , а не для идентификаторов, объявленных в исходном коде C или C++.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-118">These directives check only for the presence or absence of identifiers defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive, not for identifiers declared in the C or C++ source code.</span></span>

<span data-ttu-id="0cbfd-119">Эти директивы предназначены только для совместимости с предыдущими версиями языка.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-119">These directives are provided only for compatibility with previous versions of the language.</span></span> <span data-ttu-id="0cbfd-120">Рекомендуется использовать [определенный](dx-graphics-hlsl-appendix-pre-if.md) оператор с \# директивой if.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-120">The use of the [defined](dx-graphics-hlsl-appendix-pre-if.md) operator with the \#if directive is preferred.</span></span>

<span data-ttu-id="0cbfd-121">\#Директива ifndef проверяет наличие противоположного условия, установленного параметром \# ifdef.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-121">The \#ifndef directive checks for the opposite of the condition checked by \#ifdef.</span></span> <span data-ttu-id="0cbfd-122">Если идентификатор не определен, условие имеет значение true (не равно нулю); в противном случае условие имеет значение false (ноль).</span><span class="sxs-lookup"><span data-stu-id="0cbfd-122">If the identifier is not defined, the condition is true (nonzero); otherwise, the condition is false (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="0cbfd-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="0cbfd-123">Examples</span></span>

<span data-ttu-id="0cbfd-124">Значение идентификатора можно передать из командной строки при помощи параметра /D.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-124">The identifier can be passed from the command line using the /D option.</span></span> <span data-ttu-id="0cbfd-125">Он позволяет определить до 30 макросов.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-125">Up to 30 macros can be specified with /D.</span></span> <span data-ttu-id="0cbfd-126">Это позволяет проверить, существует ли определение, поскольку определения можно передавать из командной строки.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-126">This is useful for checking whether a definition exists, because a definition can be passed from the command line.</span></span> <span data-ttu-id="0cbfd-127">В следующем примере это поведение используется для определения того, следует ли запускать приложение в тестовом режиме.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-127">The following example uses this behavior to determine whether to run an application in test mode.</span></span>


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



<span data-ttu-id="0cbfd-128">При компиляции с помощью следующей команды Prog. cpp будет компилироваться в тестовом режиме. в противном случае он будет компилироваться в окончательном режиме.</span><span class="sxs-lookup"><span data-stu-id="0cbfd-128">When compiled using the following command, prog.cpp will compile in test mode; otherwise, it will compile in final mode.</span></span>


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a><span data-ttu-id="0cbfd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cbfd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbfd-130">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0cbfd-130">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="0cbfd-131">\#Если,)</span><span class="sxs-lookup"><span data-stu-id="0cbfd-131">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





