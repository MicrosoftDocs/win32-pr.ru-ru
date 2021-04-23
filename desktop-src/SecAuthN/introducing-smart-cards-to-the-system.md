---
description: Прежде чем подсистема смарт-карт сможет найти смарт-карту, она должна быть введена в систему.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Введение в систему смарт-карт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266245"
---
# <a name="introducing-smart-cards-to-the-system"></a><span data-ttu-id="20e96-103">Введение в систему смарт-карт</span><span class="sxs-lookup"><span data-stu-id="20e96-103">Introducing Smart Cards to the System</span></span>

<span data-ttu-id="20e96-104">Прежде чем [*подсистема смарт-карт*](../secgloss/s-gly.md) сможет найти [*смарт-карту*](../secgloss/s-gly.md), она должна быть введена в систему.</span><span class="sxs-lookup"><span data-stu-id="20e96-104">Before the [*smart card subsystem*](../secgloss/s-gly.md) can find a [*smart card*](../secgloss/s-gly.md), the smart card must be introduced to the system.</span></span> <span data-ttu-id="20e96-105">Обычно это делается с помощью средства настройки смарт-карты, предоставленного производителем карты.</span><span class="sxs-lookup"><span data-stu-id="20e96-105">This is typically done with a smart card setup tool provided by the card manufacturer.</span></span> <span data-ttu-id="20e96-106">Средство может быть программой на гибком диске (со смарт-картой), элементом управления ActiveX, доступным на веб-сайте, и т. д.</span><span class="sxs-lookup"><span data-stu-id="20e96-106">The tool could come as a program on a floppy disk (with the smart card), an ActiveX control available on a website, and so on.</span></span>

<span data-ttu-id="20e96-107">Программа установки должна предоставить следующие сведения о карточке:</span><span class="sxs-lookup"><span data-stu-id="20e96-107">The setup tool must provide the following pieces of information about the card:</span></span>

-   <span data-ttu-id="20e96-108">Его [*строка ATR*](../secgloss/a-gly.md)и необязательная маска для использования в качестве вспомогательной идентификации карты.</span><span class="sxs-lookup"><span data-stu-id="20e96-108">Its [*ATR string*](../secgloss/a-gly.md), and an optional mask to use as an aid in identifying the card.</span></span>
-   <span data-ttu-id="20e96-109">Список интерфейсов смарт-карт, поддерживаемых картой.</span><span class="sxs-lookup"><span data-stu-id="20e96-109">A list of smart card interfaces supported by the card.</span></span>
-   <span data-ttu-id="20e96-110">Отображаемое имя для карточки, используемое при определении карточки для пользователя.</span><span class="sxs-lookup"><span data-stu-id="20e96-110">A display name for the card, to be used in identifying the card to the user.</span></span> <span data-ttu-id="20e96-111">В большинстве случаев пользователь будет предоставлять его программе установки.</span><span class="sxs-lookup"><span data-stu-id="20e96-111">In most cases, the user will supply this to the setup tool.</span></span>
-   <span data-ttu-id="20e96-112">[*Основной поставщик услуг*](../secgloss/p-gly.md) , связанный с картой (необязательно) для использования при доступе к карте через интерфейсы COM.</span><span class="sxs-lookup"><span data-stu-id="20e96-112">The [*primary service provider*](../secgloss/p-gly.md) associated with the card (optional), to be used when accessing the card through COM interfaces.</span></span>

<span data-ttu-id="20e96-113">Чтобы упростить средства установки и обеспечить целостность [*базы данных смарт-карты*](../secgloss/s-gly.md), подсистема смарт-карт предоставляет следующие две функции.</span><span class="sxs-lookup"><span data-stu-id="20e96-113">To simplify setup tools, and to ensure the integrity of the [*smart card database*](../secgloss/s-gly.md), the smart card subsystem provides the following two functions.</span></span> <span data-ttu-id="20e96-114">[**Скардинтродуцекардтипе**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) вводит смарт-карту в базу данных и [**скардфоржеткардтипе**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) удаляет ее из базы данных.</span><span class="sxs-lookup"><span data-stu-id="20e96-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduces a smart card into the database and [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) removes it from the database.</span></span>

 

 
