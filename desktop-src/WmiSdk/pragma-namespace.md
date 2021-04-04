---
description: 'Запрашивает загрузку MOF-файла компилятором в пространство имен, указанное как намеспацепас. Если используются оба переключателя: компилятора MOF-n и \# pragma namespace&\# 32; намеспацепас, команда имеет приоритет над параметром.'
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: пространство имен pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811416"
---
# <a name="pragma-namespace"></a><span data-ttu-id="31ff5-104">пространство имен pragma</span><span class="sxs-lookup"><span data-stu-id="31ff5-104">pragma namespace</span></span>

<span data-ttu-id="31ff5-105">Команда препроцессора **пространства имен pragma** запрашивает, что компилятор ЗАгружает MOF-файл в пространство имен, указанное как *намеспацепас*.</span><span class="sxs-lookup"><span data-stu-id="31ff5-105">The **pragma namespace** preprocessor command requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="31ff5-106">Если используются как ключ пространства имен компилятора MOF **-n** , так и команда **\# pragma Namespace** *намеспацепас* , команда имеет приоритет над параметром.</span><span class="sxs-lookup"><span data-stu-id="31ff5-106">If both the MOF compiler **-n** namespace switch and the **\#pragma namespace** *namespacepath* command are used, the command takes priority over the switch.</span></span>

<span data-ttu-id="31ff5-107">Ниже описан синтаксис.</span><span class="sxs-lookup"><span data-stu-id="31ff5-107">The following describes the syntax:</span></span>


```mof
#pragma namespace ("[Namespace]")
```



<span data-ttu-id="31ff5-108">*\[ Пространство \] имен* — это указанное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="31ff5-108">*\[Namespace\]* is the specified namespace.</span></span>

<span data-ttu-id="31ff5-109">Если вы не укажете эту команду или эквивалентный параметр командной строки, компилятор MOF по умолчанию использует корневое \\ пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31ff5-109">If you do not specify this command or the equivalent command-line switch, the MOF compiler uses the root\\default namespace by default.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ff5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31ff5-110">Remarks</span></span>

<span data-ttu-id="31ff5-111">Можно потребовать, чтобы клиентские скрипты и приложения использовали зашифрованное соединение для проверки подлинности, добавив квалификатор **рекуиресенкриптион** в MOF-файл, который создает пространство имен.</span><span class="sxs-lookup"><span data-stu-id="31ff5-111">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="31ff5-112">Можно также изменить существующее пространство имен, добавив этот атрибут и снова скомпилировать MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="31ff5-112">You can also modify an existing namespace by adding this attribute and compile the MOF file again.</span></span> <span data-ttu-id="31ff5-113">Дополнительные сведения об использовании **рекуиресенкриптион** см. в разделе [запрос зашифрованного соединения с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="31ff5-113">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="examples"></a><span data-ttu-id="31ff5-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="31ff5-114">Examples</span></span>

<span data-ttu-id="31ff5-115">В следующем примере показано, как разместить классы или экземпляры в \\ пространстве имен "root Test".</span><span class="sxs-lookup"><span data-stu-id="31ff5-115">The following example shows how place classes or instances in the "Root\\Test" namespace.</span></span>


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a><span data-ttu-id="31ff5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="31ff5-116">Requirements</span></span>



| <span data-ttu-id="31ff5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="31ff5-117">Requirement</span></span> | <span data-ttu-id="31ff5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="31ff5-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="31ff5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31ff5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31ff5-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31ff5-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="31ff5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31ff5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31ff5-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31ff5-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31ff5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31ff5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ff5-124">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="31ff5-124">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="31ff5-125">**Стандартные квалификаторы WMI**</span><span class="sxs-lookup"><span data-stu-id="31ff5-125">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="31ff5-126">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="31ff5-126">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




