---
description: Компоненты SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Компоненты SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080359"
---
# <a name="sid-components"></a><span data-ttu-id="27f2a-103">Компоненты SID</span><span class="sxs-lookup"><span data-stu-id="27f2a-103">SID Components</span></span>

<span data-ttu-id="27f2a-104">Значение идентификатора безопасности включает компоненты, предоставляющие сведения о структуре и компонентах [**идентификатора безопасности**](/windows/desktop/api/Winnt/ns-winnt-sid) , которые однозначно идентифицируют доверенное лицо.</span><span class="sxs-lookup"><span data-stu-id="27f2a-104">A SID value includes components that provide information about the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure and components that uniquely identify a trustee.</span></span> <span data-ttu-id="27f2a-105">Идентификатор безопасности состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="27f2a-105">A SID consists of the following components:</span></span>

-   <span data-ttu-id="27f2a-106">Уровень редакции структуры [**идентификатора безопасности**](/windows/desktop/api/Winnt/ns-winnt-sid)</span><span class="sxs-lookup"><span data-stu-id="27f2a-106">The revision level of the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure</span></span>
-   <span data-ttu-id="27f2a-107">48-разрядное значение центра идентификации, идентифицирующее центр, выдавший идентификатор безопасности</span><span class="sxs-lookup"><span data-stu-id="27f2a-107">A 48-bit identifier authority value that identifies the authority that issued the SID</span></span>
-   <span data-ttu-id="27f2a-108">Переменное число значений подавтора или [*относительных идентификаторов*](/windows/desktop/SecGloss/r-gly) (RID), которые однозначно идентифицируют доверенное лицо относительно центра, который выдал идентификатор безопасности.</span><span class="sxs-lookup"><span data-stu-id="27f2a-108">A variable number of subauthority or [*relative identifier*](/windows/desktop/SecGloss/r-gly) (RID) values that uniquely identify the trustee relative to the authority that issued the SID</span></span>

<span data-ttu-id="27f2a-109">Сочетание значения центра идентификаторов и значений подавтора гарантирует, что ни один из двух идентификаторов SID не будет одинаковым, даже если два разных центра сертификации с идентификаторами безопасности выдают одно и то же сочетание значений RID.</span><span class="sxs-lookup"><span data-stu-id="27f2a-109">The combination of the identifier authority value and the subauthority values ensures that no two SIDs will be the same, even if two different SID-issuing authorities issue the same combination of RID values.</span></span> <span data-ttu-id="27f2a-110">Каждый центр, выдающий ИД безопасности, выдает определенный RID только один раз.</span><span class="sxs-lookup"><span data-stu-id="27f2a-110">Each SID-issuing authority issues a given RID only once.</span></span>

<span data-ttu-id="27f2a-111">Идентификаторы безопасности хранятся в двоичном формате в структуре [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) .</span><span class="sxs-lookup"><span data-stu-id="27f2a-111">SIDs are stored in binary format in a [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure.</span></span> <span data-ttu-id="27f2a-112">Чтобы отобразить идентификатор безопасности, можно вызвать функцию [**функция ConvertSidToStringSid вернула**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) для преобразования ДВОИЧНОГО кода SID в формат строки.</span><span class="sxs-lookup"><span data-stu-id="27f2a-112">To display a SID, you can call the [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) function to convert a binary SID to string format.</span></span> <span data-ttu-id="27f2a-113">Чтобы преобразовать строку идентификатора безопасности в допустимый, функциональный идентификатор безопасности, вызовите функцию [**конвертстрингсидтосид**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .</span><span class="sxs-lookup"><span data-stu-id="27f2a-113">To convert a SID string back to a valid, functional SID, call the [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) function.</span></span>

<span data-ttu-id="27f2a-114">Эти функции используют следующую стандартизированную строковую нотацию для идентификаторов SID, что упрощает визуализацию своих компонентов:</span><span class="sxs-lookup"><span data-stu-id="27f2a-114">These functions use the following standardized string notation for SIDs, which makes it simpler to visualize their components:</span></span>

<span data-ttu-id="27f2a-115">s-*R* - *I* - *s*...</span><span class="sxs-lookup"><span data-stu-id="27f2a-115">S-*R*-*I*-*S*…</span></span>

<span data-ttu-id="27f2a-116">В этой нотации литеральный символ "S" определяет последовательность цифр как идентификатор безопасности, *R* — уровень редакции, а *I* — это значение идентификатора авторизации и *S*...</span><span class="sxs-lookup"><span data-stu-id="27f2a-116">In this notation, the literal character "S" identifies the series of digits as a SID, *R* is the revision level, *I* is the identifier-authority value, and *S*…</span></span> <span data-ttu-id="27f2a-117">одно или несколько значений подавтора.</span><span class="sxs-lookup"><span data-stu-id="27f2a-117">is one or more subauthority values.</span></span>

<span data-ttu-id="27f2a-118">В следующем примере используется Эта нотация для вывода хорошо известного относительного домена идентификатора безопасности группы локальных администраторов:</span><span class="sxs-lookup"><span data-stu-id="27f2a-118">The following example uses this notation to display the well-known domain-relative SID of the local Administrators group:</span></span>

<span data-ttu-id="27f2a-119">S – 1-5-32-544</span><span class="sxs-lookup"><span data-stu-id="27f2a-119">S-1-5-32-544</span></span>

<span data-ttu-id="27f2a-120">В этом примере идентификатор безопасности содержит следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="27f2a-120">In this example, the SID has the following components.</span></span> <span data-ttu-id="27f2a-121">Константы в круглых скобках — это хорошо известные центры идентификации и значения [*RID*](/windows/desktop/SecGloss/r-gly) , определенные в Winnt. h:</span><span class="sxs-lookup"><span data-stu-id="27f2a-121">The constants in parentheses are well-known identifier authority and [*RID*](/windows/desktop/SecGloss/r-gly) values defined in Winnt.h:</span></span>

-   <span data-ttu-id="27f2a-122">Уровень редакции 1</span><span class="sxs-lookup"><span data-stu-id="27f2a-122">A revision level of 1</span></span>
-   <span data-ttu-id="27f2a-123">Значение ИД авторизации, равное 5 ( \_ Центр безопасности NT \_ )</span><span class="sxs-lookup"><span data-stu-id="27f2a-123">An identifier-authority value of 5 (SECURITY\_NT\_AUTHORITY)</span></span>
-   <span data-ttu-id="27f2a-124">Первое значение подавтора 32 ( \_ RID встроенного домена безопасности \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="27f2a-124">A first subauthority value of 32 (SECURITY\_BUILTIN\_DOMAIN\_RID)</span></span>
-   <span data-ttu-id="27f2a-125">Второе значение подкласса 544 ( \_ Администраторы RID псевдонима домена \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="27f2a-125">A second subauthority value of 544 (DOMAIN\_ALIAS\_RID\_ADMINS)</span></span>

 

 
