---
title: app_config Switch
description: Параметр конфигурации/АПП \_ выбирает режим настройки приложения, который позволяет использовать некоторые ключевые слова ACF в IDL-файле. С помощью этого параметра компилятора MIDL можно опустить ACF и указать интерфейс в одном IDL-файле.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config параметр MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411903"
---
# <a name="app_config-switch"></a><span data-ttu-id="636b1-105">\_параметр конфигурации/АПП</span><span class="sxs-lookup"><span data-stu-id="636b1-105">/app\_config switch</span></span>

<span data-ttu-id="636b1-106">Параметр **конфигурации \_ /АПП** выбирает режим настройки приложения, который позволяет использовать некоторые ключевые слова ACF в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="636b1-106">The **/app\_config** switch selects application-configuration mode, which allows you to use some ACF keywords in the IDL file.</span></span> <span data-ttu-id="636b1-107">С помощью этого параметра компилятора MIDL можно опустить ACF и указать интерфейс в одном IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="636b1-107">With this MIDL compiler switch, you can omit the ACF and specify an interface in a single IDL file.</span></span>

``` syntax
midl /app_config
```

## <a name="switch-options"></a><span data-ttu-id="636b1-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="636b1-108">Switch Options</span></span>

<span data-ttu-id="636b1-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="636b1-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="636b1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="636b1-110">Remarks</span></span>

<span data-ttu-id="636b1-111">Microsoft RPC поддерживает использование следующих атрибутов ACF в IDL-файле:</span><span class="sxs-lookup"><span data-stu-id="636b1-111">Microsoft RPC supports the use of the following ACF attributes in the IDL file:</span></span>

-   <span data-ttu-id="636b1-112">Неявный \_ обработчик</span><span class="sxs-lookup"><span data-stu-id="636b1-112">Implicit\_handle</span></span>
-   <span data-ttu-id="636b1-113">Автоматическая \_ работа</span><span class="sxs-lookup"><span data-stu-id="636b1-113">Auto\_handle</span></span>
-   <span data-ttu-id="636b1-114">Явный \_ маркер</span><span class="sxs-lookup"><span data-stu-id="636b1-114">Explicit\_handle</span></span>

<span data-ttu-id="636b1-115">Будущие версии Microsoft RPC могут поддерживать использование других атрибутов ACF в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="636b1-115">Future releases of Microsoft RPC may support the use of other ACF attributes in the IDL file.</span></span> <span data-ttu-id="636b1-116">Параметр **\_ конфигурации/АПП** представляет собой расширение Microsoft для спецификации использование-DCE и, как таковое, является взаимоисключающим с параметром [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="636b1-116">The **/app\_config** option represents a Microsoft extension to the OSF-DCE specification and, as such, is mutually exclusive with the [**/osf**](-osf.md) option.</span></span>

<span data-ttu-id="636b1-117">Дополнительные сведения о параметре **\_ конфигурации/АПП** см. в разделе [файл конфигурации приложения (ACF)](application-configuration-file-acf-.md) и [файл определения интерфейса (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="636b1-117">For more information related to the **/app\_config** switch, see [Application Configuration File (ACF)](application-configuration-file-acf-.md) and [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="636b1-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="636b1-118">Examples</span></span>

<span data-ttu-id="636b1-119">**MIDL/АПП \_ config filename. idl**</span><span class="sxs-lookup"><span data-stu-id="636b1-119">**midl /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="636b1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="636b1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636b1-121">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="636b1-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




