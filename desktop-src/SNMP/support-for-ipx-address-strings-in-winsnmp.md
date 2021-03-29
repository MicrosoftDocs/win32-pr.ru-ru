---
title: Поддержка строк адресов IPX в WinSNMP
description: Ошибка WinSNMP 2,0 формализация использования строк IPX-адреса.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772848"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a><span data-ttu-id="540a4-103">Поддержка строк адресов IPX в WinSNMP</span><span class="sxs-lookup"><span data-stu-id="540a4-103">Support for IPX Address Strings in WinSNMP</span></span>

<span data-ttu-id="540a4-104">Ошибка WinSNMP 2,0 формализация использования строк IPX-адреса.</span><span class="sxs-lookup"><span data-stu-id="540a4-104">WinSNMP 2.0 formalizes the use of IPX address strings.</span></span> <span data-ttu-id="540a4-105">Если указать строку IPX-адреса в качестве входного параметра для функции [**снмпстртоентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , необходимо отформатировать строку, используя следующие стандарты:</span><span class="sxs-lookup"><span data-stu-id="540a4-105">If you specify an IPX address string as an input parameter to the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function, you must format the string using the following standards:</span></span>

-   <span data-ttu-id="540a4-106">Номер сети, состоящий из восьми шестнадцатеричных цифр (при необходимости заполняется нулем)</span><span class="sxs-lookup"><span data-stu-id="540a4-106">A network number that consists of eight hexadecimal digits (zero-filled if necessary)</span></span>
-   <span data-ttu-id="540a4-107">Разделитель (":", "." или "–")</span><span class="sxs-lookup"><span data-stu-id="540a4-107">A separator (either ":", "." or " – ")</span></span>
-   <span data-ttu-id="540a4-108">Номер узла, состоящий из 12 шестнадцатеричных цифр (если это необходимо, нулевое заполнение)</span><span class="sxs-lookup"><span data-stu-id="540a4-108">A node number that consists of 12 hexadecimal digits (zero-filled if necessary)</span></span>

<span data-ttu-id="540a4-109">Например, 00000001:00081A0D01C2 или 00000001.00081 a0d01c2.</span><span class="sxs-lookup"><span data-stu-id="540a4-109">For example, 00000001:00081A0D01C2 or 00000001.00081a0d01c2.</span></span> <span data-ttu-id="540a4-110">Шестнадцатеричные цифры могут быть прописными или строчными буквами.</span><span class="sxs-lookup"><span data-stu-id="540a4-110">Hexadecimal digits can be uppercase or lowercase.</span></span>

<span data-ttu-id="540a4-111">Это формат, используемый функцией [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) для возврата строки IPX-адреса.</span><span class="sxs-lookup"><span data-stu-id="540a4-111">This is the format the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) function uses to return an IPX address string.</span></span> <span data-ttu-id="540a4-112">Строка возвращается, если приложение, работающее в одном из \_ НЕпереведенных режимов снмпапи, вызывает функцию **снмпентититостр** .</span><span class="sxs-lookup"><span data-stu-id="540a4-112">The string is returned when an application that is operating in one of the SNMPAPI\_UNTRANSLATED modes calls the **SnmpEntityToStr** function.</span></span> <span data-ttu-id="540a4-113">Строка также может возвращаться, если приложение работает в \_ режиме перевода снмпапи и для сущности не доступно понятное имя.</span><span class="sxs-lookup"><span data-stu-id="540a4-113">The string can also be returned when the application is operating in SNMPAPI\_TRANSLATED mode and no user-friendly name is available for the entity.</span></span>

 

 




