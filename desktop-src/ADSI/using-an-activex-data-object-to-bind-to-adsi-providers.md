---
title: Использование объекта данных ActiveX для привязки к поставщикам ADSI
description: Так как ADSI также является поставщиком OLE DB, для подключения к поставщикам ADSI можно использовать объект данных ActiveX (ADO).
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI объектов данных ActiveX
- Интерфейс ADSI объектов данных ActiveX использование ADO для привязки к поставщикам ADSI
- поставщики услуг ADSI, использование объекта данных ActiveX для привязки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067307"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a><span data-ttu-id="e0984-106">Использование объекта данных ActiveX для привязки к поставщикам ADSI</span><span class="sxs-lookup"><span data-stu-id="e0984-106">Using an ActiveX Data Object to Bind to ADSI Providers</span></span>

<span data-ttu-id="e0984-107">Так как ADSI также является поставщиком OLE DB, для подключения к поставщикам ADSI можно использовать объект данных ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="e0984-107">Since ADSI is also an OLE DB provider, you can use an ActiveX Data Object (ADO) to connect to ADSI providers.</span></span> <span data-ttu-id="e0984-108">Как и в случае с другими поставщиками ADO, для подключения к поставщику OLE DB необходимо создать новый объект соединения и, при необходимости, указать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e0984-108">As with other ADO providers, to connect to an OLE DB provider, you must create a new connection object and, optionally, specify the credentials.</span></span> <span data-ttu-id="e0984-109">Имя поставщика OLE DB ADSI — **адсдсубжект**.</span><span class="sxs-lookup"><span data-stu-id="e0984-109">The name of the ADSI OLE DB provider is **ADsDSOObject**.</span></span>

<span data-ttu-id="e0984-110">Пример:</span><span class="sxs-lookup"><span data-stu-id="e0984-110">For example:</span></span>


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



<span data-ttu-id="e0984-111">В предыдущем примере вы подключены от имени текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="e0984-111">In the previous example, you are connected on behalf of the current user.</span></span> <span data-ttu-id="e0984-112">Чтобы указать другие учетные данные, используйте свойства соединения:</span><span class="sxs-lookup"><span data-stu-id="e0984-112">To specify different credentials, use connection properties:</span></span>


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



<span data-ttu-id="e0984-113">ADSI OLE DB определяет следующие свойства соединения.</span><span class="sxs-lookup"><span data-stu-id="e0984-113">ADSI OLE DB defines the following connection properties.</span></span>



| <span data-ttu-id="e0984-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="e0984-114">Property</span></span>           | <span data-ttu-id="e0984-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e0984-115">Data type</span></span>   | <span data-ttu-id="e0984-116">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e0984-116">Default</span></span>   |
|--------------------|-------------|-----------|
| <span data-ttu-id="e0984-117">"Идентификатор пользователя"</span><span class="sxs-lookup"><span data-stu-id="e0984-117">"User ID"</span></span>          | <span data-ttu-id="e0984-118">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="e0984-118">**BSTR**</span></span>    | <span data-ttu-id="e0984-119">**NULL**</span><span class="sxs-lookup"><span data-stu-id="e0984-119">**NULL**</span></span>  |
| <span data-ttu-id="e0984-120">"Пароль".</span><span class="sxs-lookup"><span data-stu-id="e0984-120">"Password"</span></span>         | <span data-ttu-id="e0984-121">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="e0984-121">**BSTR**</span></span>    | <span data-ttu-id="e0984-122">**NULL**</span><span class="sxs-lookup"><span data-stu-id="e0984-122">**NULL**</span></span>  |
| <span data-ttu-id="e0984-123">"Зашифровать пароль"</span><span class="sxs-lookup"><span data-stu-id="e0984-123">"Encrypt Password"</span></span> | <span data-ttu-id="e0984-124">**BOOLEAN**</span><span class="sxs-lookup"><span data-stu-id="e0984-124">**BOOLEAN**</span></span> | <span data-ttu-id="e0984-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="e0984-125">**FALSE**</span></span> |
| <span data-ttu-id="e0984-126">"Флаг ADSI"</span><span class="sxs-lookup"><span data-stu-id="e0984-126">"ADSI Flag"</span></span>        | <span data-ttu-id="e0984-127">**Long**</span><span class="sxs-lookup"><span data-stu-id="e0984-127">**Long**</span></span>    | <span data-ttu-id="e0984-128">0</span><span class="sxs-lookup"><span data-stu-id="e0984-128">0</span></span>         |



 

<span data-ttu-id="e0984-129">С помощью OLE DB ADO невозможно выполнить привязку к определенному объекту.</span><span class="sxs-lookup"><span data-stu-id="e0984-129">Using OLE DB ADO, you cannot bind to a specific object.</span></span> <span data-ttu-id="e0984-130">Однако можно запросить конкретный объект и возвратить результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="e0984-130">You can, however, query a specific object and get a result set back.</span></span> <span data-ttu-id="e0984-131">Только поставщики ADSI, которые поддерживают [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , имеют преимущества от использования ADO в качестве модели программирования.</span><span class="sxs-lookup"><span data-stu-id="e0984-131">Only ADSI providers that support [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefit from having ADO as a programming model.</span></span>

<span data-ttu-id="e0984-132">Свойство флага ADSI используется для указания параметра проверки подлинности привязки.</span><span class="sxs-lookup"><span data-stu-id="e0984-132">The ADSI Flag property is used to specify the binding authentication option.</span></span> <span data-ttu-id="e0984-133">Это свойство может быть сочетанием флагов из перечисления [**объявлений \_ проверки \_ подлинности**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .</span><span class="sxs-lookup"><span data-stu-id="e0984-133">This property can be a combination of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration.</span></span>

 

 




