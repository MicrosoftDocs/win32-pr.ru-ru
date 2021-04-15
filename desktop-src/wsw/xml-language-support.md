---
title: Поддержка языка XML
description: В этом разделе описывается уровень поддержки языка XML в WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Веб-службы поддержки языка XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105661795"
---
# <a name="xml-language-support"></a><span data-ttu-id="2bdaf-106">Поддержка языка XML</span><span class="sxs-lookup"><span data-stu-id="2bdaf-106">XML Language Support</span></span>

<span data-ttu-id="2bdaf-107">В этом разделе описывается уровень поддержки языка XML в WWS.</span><span class="sxs-lookup"><span data-stu-id="2bdaf-107">This section describe level of XML Language support in WWS.</span></span>


<span data-ttu-id="2bdaf-108">Ознакомьтесь с функциями ДовнлевеллЦидтолокаленаме в версиях Windows, предшествующих Windows Vista, и ЛЦидтолокалнаме в противном случае, чтобы преобразовать значения LCID в значение XML: lang.</span><span class="sxs-lookup"><span data-stu-id="2bdaf-108">See the functions DownlevelLCIDToLocaleName on versions of Windows earlier than Windows Vista, and LCIDToLocalName otherwise, to convert between an LCID and an xml:lang value.</span></span>

<span data-ttu-id="2bdaf-109">При чтении [**всжетксмлаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) может использоваться для обнаружения значения атрибута "XML: lang" в области.</span><span class="sxs-lookup"><span data-stu-id="2bdaf-109">When reading, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) may be used to discover the value of an "xml:lang" attribute in scope.</span></span>

<span data-ttu-id="2bdaf-110">При записи [**всвритестартаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) может использоваться для записи атрибута "XML: lang".</span><span class="sxs-lookup"><span data-stu-id="2bdaf-110">When writing, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) may be used to write an "xml:lang" attribute.</span></span>

 

 




