---
description: В этом разделе описывается инициализация диспетчера подписей для использования с документом XPS.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Инициализация диспетчера сигнатур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719708"
---
# <a name="initialize-the-signature-manager"></a><span data-ttu-id="ae0cf-103">Инициализация диспетчера сигнатур</span><span class="sxs-lookup"><span data-stu-id="ae0cf-103">Initialize the Signature Manager</span></span>

<span data-ttu-id="ae0cf-104">В этом разделе описывается инициализация диспетчера подписей для использования с документом XPS.</span><span class="sxs-lookup"><span data-stu-id="ae0cf-104">This topic describes how to initialize the signature manager for use with an XPS document.</span></span>

<span data-ttu-id="ae0cf-105">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ae0cf-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="ae0cf-106">Чтобы использовать функции Windows 7 API шифрования, определите для параметра "шифрование **\_ OID" \_ \_ \_ Дополнительные \_ поля** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae0cf-106">To use the Windows 7 features of the Crypto API, define the **CRYPT\_OID\_INFO\_HAS\_EXTRA\_FIELDS** symbol as follows:</span></span>


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



<span data-ttu-id="ae0cf-107">Затем создайте экземпляр интерфейса [**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) , вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="ae0cf-107">Next, instantiate an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), as shown in the following code example.</span></span>


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



<span data-ttu-id="ae0cf-108">Интерфейс, созданный с помощью [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , может использоваться только одним документом XPS, который должен быть загружен путем вызова [**лоадпаккажефиле**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) или [**лоадпаккажестреам**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) перед вызовом любого другого метода.</span><span class="sxs-lookup"><span data-stu-id="ae0cf-108">The interface instantiated by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) can be used by only one XPS document, which must be loaded by calling [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) before calling any other method.</span></span>

<span data-ttu-id="ae0cf-109">После создания экземпляра интерфейса [**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) и загрузки XPS-документа диспетчер подписей готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="ae0cf-109">After the [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae0cf-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ae0cf-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ae0cf-111">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="ae0cf-111">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="ae0cf-112">Подписать документ</span><span class="sxs-lookup"><span data-stu-id="ae0cf-112">Sign a Document</span></span>](sign-a-document.md)
</dt> <dt>

[<span data-ttu-id="ae0cf-113">Добавление запроса подписи в документ XPS</span><span class="sxs-lookup"><span data-stu-id="ae0cf-113">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="ae0cf-114">Проверка подписей документов</span><span class="sxs-lookup"><span data-stu-id="ae0cf-114">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="ae0cf-115">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="ae0cf-115">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="ae0cf-116">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ae0cf-116">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="ae0cf-117">**икспссигнатуреманажер**</span><span class="sxs-lookup"><span data-stu-id="ae0cf-117">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

<span data-ttu-id="ae0cf-118">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="ae0cf-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="ae0cf-119">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="ae0cf-119">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="ae0cf-120">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="ae0cf-120">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="ae0cf-121">XPS</span><span class="sxs-lookup"><span data-stu-id="ae0cf-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
