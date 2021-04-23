---
title: Текст ACF
description: Текст ACF содержит атрибуты конфигурации, которые применяются к типам и функциям, определенным в теле интерфейса IDL-файла.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104070769"
---
# <a name="the-acf-body"></a><span data-ttu-id="fc5b2-103">Текст ACF</span><span class="sxs-lookup"><span data-stu-id="fc5b2-103">The ACF Body</span></span>

<span data-ttu-id="fc5b2-104">Текст ACF содержит атрибуты конфигурации, которые применяются к типам и функциям, определенным в теле интерфейса IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-104">The ACF body contains configuration attributes that apply to types and functions defined in the interface body of the IDL file.</span></span> <span data-ttu-id="fc5b2-105">Тело ACF может быть пустым или содержать атрибуты ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), Function и Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-105">The body of the ACF can be empty or it can contain ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), function, and parameter attributes.</span></span> <span data-ttu-id="fc5b2-106">Все эти элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-106">All of these items are optional.</span></span> <span data-ttu-id="fc5b2-107">Атрибуты, применяемые к отдельным типам и функциям в теле ACF, переопределяют атрибуты в заголовке ACF.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-107">Attributes applied to individual types and functions in the ACF body override attributes in the ACF header.</span></span>

<span data-ttu-id="fc5b2-108">ACF указывает поведение на локальном компьютере и не влияет на данные, передаваемые по сети.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-108">The ACF specifies behavior on the local computer and does not affect the data transmitted over the network.</span></span> <span data-ttu-id="fc5b2-109">Он используется для указания сведений о создаваемой заглушке.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-109">It is used to specify details of a stub to be generated.</span></span> <span data-ttu-id="fc5b2-110">В режиме совместимости с DCE ([**/ОСФ**](/windows/desktop/Midl/-osf)) ACF не влияет на взаимодействие между заглушками, но между заглушкой и кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-110">In DCE-compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), the ACF does not affect interaction between stubs, but between the stub and application code.</span></span>

<span data-ttu-id="fc5b2-111">Параметр, указанный в ACF, должен быть одним из параметров, указанных в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-111">A parameter specified in the ACF must be one of the parameters specified in the IDL file.</span></span> <span data-ttu-id="fc5b2-112">Порядок спецификации параметра в ACF не имеет значения, так как сопоставление выполняется по имени, а не по положению.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-112">The order of specification of the parameter in the ACF is not significant because the matching is by name, not by position.</span></span> <span data-ttu-id="fc5b2-113">Список параметров в ACF может быть пустым, даже если список параметров в соответствующей сигнатуре IDL не имеет значение (но это не рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="fc5b2-113">The parameter list in the ACF can be empty, even when the parameter list in the corresponding IDL signature is not (but this is not recommended).</span></span> <span data-ttu-id="fc5b2-114">Абстрактные деклараторы (неименованные параметры) в IDL-файле приводят к тому, что компилятор MIDL сообщает об ошибках при обработке ACF, так как параметр не найден.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-114">Abstract declarators (unnamed parameters) in the IDL file cause the MIDL compiler to report errors while processing the ACF because the parameter is not found.</span></span>

<span data-ttu-id="fc5b2-115">Директива **include** ACF указывает файлы заголовков, которые будут отображаться в созданном заголовке как часть **\# стандартной инструкции-** препроцессора C.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-115">The ACF **include** directive specifies the header files to appear in the generated header as part of a standard C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="fc5b2-116">Ключевое слово ACF **содержит** отличия от директивы **\# include** .</span><span class="sxs-lookup"><span data-stu-id="fc5b2-116">The ACF keyword **include** differs from an **\#include** directive.</span></span> <span data-ttu-id="fc5b2-117">Ключевое слово **ACF включает в себя включение** отображения строки "**\# include** *filename*" в создаваемом файле заголовка, а директива языка C — "include filename" (**\# Включение** *имени* файла) приводит к тому, что содержимое этого файла помещается в ACF.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-117">The ACF keyword **include** causes the line "**\#include** *filename*" to appear in the generated header file, while the C-language directive "**\#include** *filename*" causes the contents of that file to be placed in the ACF.</span></span>

<span data-ttu-id="fc5b2-118">Инструкция ACF [**typedef**](/windows/desktop/Midl/typedef) позволяет применять АТРИБУТЫ типа ACF к типам, ранее определенным в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-118">The ACF [**typedef**](/windows/desktop/Midl/typedef) statement lets you apply ACF type attributes to types previously defined in the IDL file.</span></span> <span data-ttu-id="fc5b2-119">Синтаксис **TYPEDEF** ACF отличается от синтаксиса с **typedef** .</span><span class="sxs-lookup"><span data-stu-id="fc5b2-119">The ACF **typedef** syntax differs from the C **typedef** syntax.</span></span>

<span data-ttu-id="fc5b2-120">Атрибуты функции ACF позволяют указать атрибуты, которые применяются к функции в целом.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-120">The ACF function attributes let you specify attributes that apply to the function as a whole.</span></span> <span data-ttu-id="fc5b2-121">Дополнительные сведения см. в разделе **\[** [**код**](/windows/desktop/Midl/code) **\]** , **\[** [**Оптимизация**](/windows/desktop/Midl/optimize) **\]** и **\[** [**некод**](/windows/desktop/Midl/nocode) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fc5b2-121">For more information, see **\[**[**code**](/windows/desktop/Midl/code)**\]**, **\[**[**optimize**](/windows/desktop/Midl/optimize)**\]**, and **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]**.</span></span>

<span data-ttu-id="fc5b2-122">Атрибуты параметра ACF позволяют указать атрибуты, которые применяются к отдельным параметрам функции.</span><span class="sxs-lookup"><span data-stu-id="fc5b2-122">The ACF parameter attributes let you specify attributes that apply to individual parameters of the function.</span></span> <span data-ttu-id="fc5b2-123">Дополнительные сведения см. в разделе **\[** [**\_ число байтов**](/windows/desktop/Midl/byte-count) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fc5b2-123">For more information, see **\[**[**byte\_count**](/windows/desktop/Midl/byte-count)**\]**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc5b2-124">См. также</span><span class="sxs-lookup"><span data-stu-id="fc5b2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc5b2-125">**\_Конфигурация/АПП**</span><span class="sxs-lookup"><span data-stu-id="fc5b2-125">**/app\_config**</span></span>](/windows/desktop/Midl/-app-config)
</dt> <dt>

[<span data-ttu-id="fc5b2-126">**/осф**</span><span class="sxs-lookup"><span data-stu-id="fc5b2-126">**/osf**</span></span>](/windows/desktop/Midl/-osf)
</dt> <dt>

<span data-ttu-id="fc5b2-127">[**\[Автоматическая \_ работа\]**](../midl/auto-handle.md)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-127">[**\[auto\_handle\]**](../midl/auto-handle.md)</span></span>
</dt> <dt>

<span data-ttu-id="fc5b2-128">[**\[приведен\]**](../midl/code.md)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-128">[**\[code\]**](../midl/code.md)</span></span>
</dt> <dt>

<span data-ttu-id="fc5b2-129">[**\[явный \_ маркер\]**](../midl/explicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-129">[**\[explicit\_handle\]**](../midl/explicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="fc5b2-130">Файл языка определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-130">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
</dt> <dt>

<span data-ttu-id="fc5b2-131">[**\[неявный \_ обработчик\]**](../midl/implicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-131">[**\[implicit\_handle\]**](../midl/implicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="fc5b2-132">**относится**</span><span class="sxs-lookup"><span data-stu-id="fc5b2-132">**include**</span></span>](/windows/desktop/Midl/include)
</dt> <dt>

[<span data-ttu-id="fc5b2-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="fc5b2-133">midl</span></span>](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

<span data-ttu-id="fc5b2-134">[**\[nocode\]**](../midl/nocode.md)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-134">[**\[nocode\]**](../midl/nocode.md)</span></span>
</dt> <dt>

<span data-ttu-id="fc5b2-135">[**\[увеличить\]**](../midl/optimize.md)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-135">[**\[optimize\]**](../midl/optimize.md)</span></span>
</dt> <dt>

<span data-ttu-id="fc5b2-136">[**\[представлять \_ как\]**](../midl/represent-as.md)</span><span class="sxs-lookup"><span data-stu-id="fc5b2-136">[**\[represent\_as\]**](../midl/represent-as.md)</span></span>
</dt> <dt>

[<span data-ttu-id="fc5b2-137">**определение**</span><span class="sxs-lookup"><span data-stu-id="fc5b2-137">**typedef**</span></span>](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 