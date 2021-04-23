---
title: дллсуррогате
description: Позволяет серверам DLL выполняться в суррогатном процессе. Если указана пустая строка, используется заданный системой суррогат; в противном случае значение указывает путь к используемому суррогату.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- COM-значение реестра Дллсуррогате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413825"
---
# <a name="dllsurrogate"></a><span data-ttu-id="68e89-105">дллсуррогате</span><span class="sxs-lookup"><span data-stu-id="68e89-105">DllSurrogate</span></span>

<span data-ttu-id="68e89-106">Позволяет серверам DLL выполняться в суррогатном процессе.</span><span class="sxs-lookup"><span data-stu-id="68e89-106">Enables DLL servers to run in a surrogate process.</span></span> <span data-ttu-id="68e89-107">Если указана пустая строка, используется заданный системой суррогат; в противном случае значение указывает путь к используемому суррогату.</span><span class="sxs-lookup"><span data-stu-id="68e89-107">If an empty string is specified, the system-supplied surrogate is used; otherwise, the value specifies the path of the surrogate to be used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="68e89-108">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="68e89-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a><span data-ttu-id="68e89-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68e89-109">Remarks</span></span>

<span data-ttu-id="68e89-110">Это значение **reg \_ SZ** , указывающее, что класс является библиотекой DLL, которая должна быть активирована в суррогатном процессе, и используемый суррогатный процесс.</span><span class="sxs-lookup"><span data-stu-id="68e89-110">This is a **REG\_SZ** value that specifies that the class is a DLL that is to be activated in a surrogate process, and the surrogate process to be used.</span></span> <span data-ttu-id="68e89-111">Чтобы использовать заданный системой универсальный суррогатный процесс, задайте для *path* пустую строку или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="68e89-111">To use the system-supplied generic surrogate process, set *path* to an empty string or **NULL**.</span></span> <span data-ttu-id="68e89-112">Чтобы указать другой суррогатный процесс, задайте *путь* к пути суррогата.</span><span class="sxs-lookup"><span data-stu-id="68e89-112">To specify another surrogate process, set *path* to the path of the surrogate.</span></span> <span data-ttu-id="68e89-113">Как и в спецификации пути к серверу в разделе [**LocalServer32**](localserver32.md) , полное указание пути не требуется.</span><span class="sxs-lookup"><span data-stu-id="68e89-113">As in the specification of the path of a server under the [**LocalServer32**](localserver32.md) key, a full path specification is not necessary.</span></span> <span data-ttu-id="68e89-114">Суррогат должен быть написан для правильной связи со службой DCOM, как описано в разделе [написание пользовательского суррогата](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="68e89-114">The surrogate must be written to properly communicate with the DCOM service as described in [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

<span data-ttu-id="68e89-115">Значение **дллсуррогате** должно присутствовать для активизации сервера DLL в суррогате.</span><span class="sxs-lookup"><span data-stu-id="68e89-115">The **DllSurrogate** value must be present for a DLL server to be activated in a surrogate.</span></span> <span data-ttu-id="68e89-116">Активация относится к вызову [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**кокреатеинстанцеекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **кокреатеинстанцеекс**, [**Кожетинстанцефромфиле**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**кожетинстанцефромистораже**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)или [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="68e89-116">Activation refers to a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage), or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="68e89-117">Выполнение библиотек DLL в суррогатном процессе предоставляет преимущества реализации исполняемого файла, включая изоляцию отказа, возможность одновременного обслуживания нескольких клиентов и предоставление серверу возможности предоставлять службы удаленным клиентам в распределенной среде.</span><span class="sxs-lookup"><span data-stu-id="68e89-117">Running DLLs in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68e89-118">См. также</span><span class="sxs-lookup"><span data-stu-id="68e89-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68e89-119">**корегистерсуррогате**</span><span class="sxs-lookup"><span data-stu-id="68e89-119">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="68e89-120">Суррогаты библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="68e89-120">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="68e89-121">**дллсуррогатиксекутабле**</span><span class="sxs-lookup"><span data-stu-id="68e89-121">**DllSurrogateExecutable**</span></span>](dllsurrogateexecutable.md)
</dt> <dt>

[<span data-ttu-id="68e89-122">**исуррогате**</span><span class="sxs-lookup"><span data-stu-id="68e89-122">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 