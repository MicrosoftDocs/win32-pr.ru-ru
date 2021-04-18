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
# <a name="initialize-the-signature-manager"></a>Инициализация диспетчера сигнатур

В этом разделе описывается инициализация диспетчера подписей для использования с документом XPS.

Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).

Чтобы использовать функции Windows 7 API шифрования, определите для параметра "шифрование **\_ OID" \_ \_ \_ Дополнительные \_ поля** следующим образом:


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



Затем создайте экземпляр интерфейса [**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) , вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), как показано в следующем примере кода.


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



Интерфейс, созданный с помощью [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , может использоваться только одним документом XPS, который должен быть загружен путем вызова [**лоадпаккажефиле**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) или [**лоадпаккажестреам**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) перед вызовом любого другого метода.

После создания экземпляра интерфейса [**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) и загрузки XPS-документа диспетчер подписей готов к использованию.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Подписать документ](sign-a-document.md)
</dt> <dt>

[Добавление запроса подписи в документ XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Проверка подписей документов](verify-document-signatures.md)
</dt> <dt>

**Используется в этом разделе**
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Ошибки API цифровой подписи XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Ошибки документа XPS](xps-document-errors.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
