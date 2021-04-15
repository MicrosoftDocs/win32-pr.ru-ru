---
description: '\_Свойство NewEnum сертификатов Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 71760f23bbb19d32c3caf8011eb87b8d03941eac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689404"
---
# <a name="certificates_newenum-property"></a><span data-ttu-id="0735c-104">Сертификаты. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="0735c-104">Certificates.\_NewEnum property</span></span>

<span data-ttu-id="0735c-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0735c-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0735c-106">Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0735c-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0735c-107">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="0735c-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="0735c-108">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="0735c-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="0735c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0735c-109">Syntax</span></span>


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="0735c-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0735c-110">Property value</span></span>

<span data-ttu-id="0735c-111">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="0735c-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0735c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0735c-112">Remarks</span></span>

<span data-ttu-id="0735c-113">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="0735c-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="0735c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0735c-114">Requirements</span></span>



| <span data-ttu-id="0735c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0735c-115">Requirement</span></span> | <span data-ttu-id="0735c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0735c-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0735c-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0735c-117">End of client support</span></span><br/> | <span data-ttu-id="0735c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0735c-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0735c-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0735c-119">End of server support</span></span><br/> | <span data-ttu-id="0735c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0735c-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0735c-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0735c-121">Redistributable</span></span><br/>       | <span data-ttu-id="0735c-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0735c-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0735c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0735c-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0735c-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0735c-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0735c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0735c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0735c-126">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="0735c-126">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
