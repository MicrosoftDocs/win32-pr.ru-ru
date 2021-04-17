---
description: При вызове функции Креатепипе можно указать дескриптор безопасности для анонимного канала. Дескриптор безопасности управляет доступом к концам канала чтения и записи.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Безопасность анонимных каналов и права доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684427"
---
# <a name="anonymous-pipe-security-and-access-rights"></a><span data-ttu-id="c9ff6-104">Безопасность анонимных каналов и права доступа</span><span class="sxs-lookup"><span data-stu-id="c9ff6-104">Anonymous Pipe Security and Access Rights</span></span>

<span data-ttu-id="c9ff6-105">Система безопасности Windows позволяет управлять доступом к анонимным каналам.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-105">Windows security enables you to control access to anonymous pipes.</span></span> <span data-ttu-id="c9ff6-106">Дополнительные сведения о безопасности см. в разделе [модель управления доступом](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="c9ff6-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="c9ff6-107">При вызове функции [**креатепипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) можно указать [дескриптор безопасности](/windows/desktop/SecAuthZ/security-descriptors) для канала.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a pipe when you call the [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function.</span></span> <span data-ttu-id="c9ff6-108">Дескриптор безопасности управляет доступом к концам канала чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-108">The security descriptor controls access to both the read and write ends of the pipe.</span></span> <span data-ttu-id="c9ff6-109">Если указано **значение NULL**, то канал получает дескриптор безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-109">If you specify **NULL**, the pipe gets a default security descriptor.</span></span> <span data-ttu-id="c9ff6-110">Списки ACL в дескрипторе безопасности по умолчанию для канала берутся из основного маркера или токена олицетворения создателя.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-110">The ACLs in the default security descriptor for a pipe come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="c9ff6-111">Чтобы получить дескриптор безопасности канала, вызовите функцию [**жетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="c9ff6-111">To retrieve a pipe's security descriptor, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span> <span data-ttu-id="c9ff6-112">Чтобы изменить дескриптор безопасности канала, вызовите функцию [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="c9ff6-112">To change a pipe's security descriptor, call the [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) function.</span></span>

<span data-ttu-id="c9ff6-113">Функция [**креатепипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) возвращает два дескриптора для анонимного канала: дескриптор чтения с универсальным \_ доступом для чтения и синхронизации, а также дескриптор записи с универсальным \_ доступом для записи и синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-113">The [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function returns two handles to the anonymous pipe: a read handle with GENERIC\_READ and SYNCHRONIZE access; and a write handle with GENERIC\_WRITE and SYNCHRONIZE access.</span></span> <span data-ttu-id="c9ff6-114">УНИВЕРСАЛЬНое \_ чтение и общий \_ доступ на запись используют те же права доступа, что и для именованных каналов.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-114">GENERIC\_READ and GENERIC\_WRITE access use the same access rights mapping as for named pipes.</span></span>

<span data-ttu-id="c9ff6-115">УНИВЕРСАЛЬНЫЙ \_ доступ на чтение для анонимного канала объединяет права на чтение данных из канала, чтение атрибутов канала, чтение расширенных атрибутов и чтение списка DACL канала.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-115">GENERIC\_READ access for an anonymous pipe combines the rights to read data from the pipe, read pipe attributes, read extended attributes, and read the pipe's DACL.</span></span>

<span data-ttu-id="c9ff6-116">УНИВЕРСАЛЬНЫЙ \_ доступ на запись для анонимного канала объединяет права на запись данных в канал, добавляет к нему данные, записывает атрибуты канала, записывает расширенные атрибуты и считывает список DACL канала.</span><span class="sxs-lookup"><span data-stu-id="c9ff6-116">GENERIC\_WRITE access for an anonymous pipe combines the rights to write data to the pipe, append data to it, write pipe attributes, write extended attributes, and read the pipe's DACL.</span></span>

 

 
