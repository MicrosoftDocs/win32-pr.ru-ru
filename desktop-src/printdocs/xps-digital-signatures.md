---
description: API цифровой подписи XPS позволяет пользователю подписать документ, проверить удостоверение подписавшего и указать, изменился ли документ XPS с момента подписания.
ms.assetid: 8a23617e-92fe-4662-b602-47add5716358
title: API цифровой подписи XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c56485a532afbb148e62901c38db49ab81963c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684295"
---
# <a name="xps-digital-signature-api"></a><span data-ttu-id="abf57-103">API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="abf57-103">XPS Digital Signature API</span></span>

<span data-ttu-id="abf57-104">API цифровой подписи XPS позволяет пользователю подписать документ, проверить удостоверение подписавшего и указать, изменился ли документ XPS с момента подписания.</span><span class="sxs-lookup"><span data-stu-id="abf57-104">The XPS Digital Signature API enables a user to sign a document, verify the identity of the signer, and indicate whether an XPS document has changed since it was signed.</span></span> <span data-ttu-id="abf57-105">API цифровой подписи XPS основан на технологии цифровой подписи, которая используется в соглашениях Open Packaging, которые указаны в первом выпуске, часть 2, «Open Packaging Conventions» [стандартных форматов файлов ECMA-376, Office Open XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span><span class="sxs-lookup"><span data-stu-id="abf57-105">The XPS Digital Signature API is built on the digital signature technology that is used in the Open Packaging Conventions, which are specified in the 1st edition, Part 2, "Open Packaging Conventions," of [Standard ECMA-376, Office Open XML File Formats](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="abf57-106">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="abf57-106">In This Section</span></span>

<span data-ttu-id="abf57-107">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="abf57-107">This section contains the following topics.</span></span>

### <a name="about-xps-digital-signature-api"></a><span data-ttu-id="abf57-108">О API цифровых подписей XPS</span><span class="sxs-lookup"><span data-stu-id="abf57-108">About XPS Digital Signature API</span></span>

<span data-ttu-id="abf57-109">[О API цифровой подписи XPS](about-xps-digital-signatures.md) описывается интерфейс API цифровой подписи XPS на высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="abf57-109">[About XPS Digital Signature API](about-xps-digital-signatures.md) describes the XPS Digital Signature API at a high level.</span></span>

### <a name="using-xps-digital-signature-api"></a><span data-ttu-id="abf57-110">Использование API цифровых подписей XPS</span><span class="sxs-lookup"><span data-stu-id="abf57-110">Using XPS Digital Signature API</span></span>

<span data-ttu-id="abf57-111">[Использование API цифровых подписей XPS](using-digital-signatures-in-xps-documents.md) описание использования API цифровой подписи XPS.</span><span class="sxs-lookup"><span data-stu-id="abf57-111">[Using XPS Digital Signature API](using-digital-signatures-in-xps-documents.md) describes how to use the XPS Digital Signature API.</span></span>

### <a name="xps-digital-signatures-reference"></a><span data-ttu-id="abf57-112">Справочник по цифровым подписям XPS</span><span class="sxs-lookup"><span data-stu-id="abf57-112">XPS Digital Signatures Reference</span></span>

<span data-ttu-id="abf57-113">[Справочник по API цифровых](xps-digital-signatures-programming-reference.md) подписей XPS содержит полный список интерфейсов, методов и перечислителей, реализованных с помощью API цифровых подписей XPS.</span><span class="sxs-lookup"><span data-stu-id="abf57-113">The [XPS Digital Signature API Reference](xps-digital-signatures-programming-reference.md) contains a complete listing of the interfaces, methods, and enumerators that are implemented by the XPS Digital Signatures API.</span></span>

## <a name="platform-update-for-windows-vista"></a><span data-ttu-id="abf57-114">Обновление платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abf57-114">Platform Update for Windows Vista</span></span>

<span data-ttu-id="abf57-115">Интерфейсы цифровой подписи XPS, описанные в этом разделе, не поддерживаются обновлением платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="abf57-115">The XPS Digital Signature interfaces that are described in this section are not supported by the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="abf57-116">Приложение, которому требуются эти интерфейсы, должно выполняться в Windows 7 или более поздней версии или в Windows Server 2008 R2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="abf57-116">An application that requires these interfaces should run on Windows 7 or later, or on Windows Server 2008 R2 or later.</span></span> <span data-ttu-id="abf57-117">В противном случае приложение может не предоставить пользователю полную функциональность приложения.</span><span class="sxs-lookup"><span data-stu-id="abf57-117">Otherwise, the application may not provide the user with the application's complete functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abf57-118">См. также</span><span class="sxs-lookup"><span data-stu-id="abf57-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abf57-119">Упаковка</span><span class="sxs-lookup"><span data-stu-id="abf57-119">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="abf57-120">XPS</span><span class="sxs-lookup"><span data-stu-id="abf57-120">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="abf57-121">Стандартные ECMA-376, форматы файлов Office Open XML</span><span class="sxs-lookup"><span data-stu-id="abf57-121">Standard ECMA-376, Office Open XML File Formats</span></span>](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
