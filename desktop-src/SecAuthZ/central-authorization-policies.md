---
description: Централизованная политика авторизации (CAP) собирает определенные правила авторизации (Капрс) в единую политику.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Централизованные политики авторизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647221"
---
# <a name="central-authorization-policies"></a><span data-ttu-id="29eab-103">Централизованные политики авторизации</span><span class="sxs-lookup"><span data-stu-id="29eab-103">Central Authorization Policies</span></span>

<span data-ttu-id="29eab-104">Централизованная политика авторизации (CAP) собирает определенные правила авторизации (Капрс) в единую политику.</span><span class="sxs-lookup"><span data-stu-id="29eab-104">A Central Authorization Policy (CAP) collects the specific authorization rules (CAPRs) into a single policy.</span></span> <span data-ttu-id="29eab-105">Чтобы обеспечить объединение конкретных правил авторизации (Капрс) в целостную политику авторизации Организации, на Капрс можно ссылаться вместе и применять к набору ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29eab-105">To allow the specific authorization rules (CAPRs) to be combined into the holistic authorization policy of the organization, CAPRs can be referenced together and applied to a set of resources.</span></span> <span data-ttu-id="29eab-106">Для этого выполняется сбор нескольких (по ссылке) в конец.</span><span class="sxs-lookup"><span data-stu-id="29eab-106">This is done by collecting multiple (by reference) into a CAP.</span></span> <span data-ttu-id="29eab-107">После определения ограничения его можно распределить с помощью диспетчеров ресурсов, чтобы применить политику авторизации организаций к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="29eab-107">Once a CAP is defined it can be distributed consumed by resource managers to apply the organizations authorization policy to resources.</span></span>

<span data-ttu-id="29eab-108">ОГРАНИЧЕНИЕ имеет следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="29eab-108">A CAP has the following attributes:</span></span>

-   <span data-ttu-id="29eab-109">Коллекция Капрс — список ссылок на существующие объекты КАПР</span><span class="sxs-lookup"><span data-stu-id="29eab-109">Collection of CAPRs – a list of references to existing CAPR objects</span></span>
-   <span data-ttu-id="29eab-110">Идентификатор (SID)</span><span class="sxs-lookup"><span data-stu-id="29eab-110">An identifier (Sid)</span></span>
-   <span data-ttu-id="29eab-111">Описание</span><span class="sxs-lookup"><span data-stu-id="29eab-111">Description</span></span>
-   <span data-ttu-id="29eab-112">Имя</span><span class="sxs-lookup"><span data-stu-id="29eab-112">Name</span></span>

<span data-ttu-id="29eab-113">ОГРАНИЧЕНИЕ оценивается во время оценки доступа к файлам и папкам, которые включает администратор.</span><span class="sxs-lookup"><span data-stu-id="29eab-113">A CAP is evaluated during access evaluation for files and folders on which an administrator enables it.</span></span> <span data-ttu-id="29eab-114">Во время вызова [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) проверка ограничения логически сочетается с избирательной проверками ACL. Это означает, что для получения доступа к файлу, к которому применяется ограничение, пользователю необходимо получить доступ в соответствии с ОГРАНИЧЕНИЕм (связанным с ним Капрс) и избирательным ACL для файла.</span><span class="sxs-lookup"><span data-stu-id="29eab-114">During an [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) call, the CAP check is logically combined with the discretionary ACL check; this means that in order to obtain access to a file to which the CAP applies, a user needs to have access both according to the CAP (its associated CAPRs) and the discretionary ACL on the file.</span></span>

<span data-ttu-id="29eab-115">Пример конца:</span><span class="sxs-lookup"><span data-stu-id="29eab-115">Example CAP:</span></span>

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a><span data-ttu-id="29eab-116">Определение ограничения</span><span class="sxs-lookup"><span data-stu-id="29eab-116">CAP Definition</span></span>

<span data-ttu-id="29eab-117">Политика создается и редактируется в Active Directory с помощью нового UX в ADAC (или PowerShell), который позволяет администратору создать ограничение и указать набор Капрс, составляющих ограничение.</span><span class="sxs-lookup"><span data-stu-id="29eab-117">A CAP is created and edited in Active Directory using a new UX in ADAC (or PowerShell) that allows the administrator to create a CAP and specify a set of CAPRs that make up the CAP.</span></span>

 

 
