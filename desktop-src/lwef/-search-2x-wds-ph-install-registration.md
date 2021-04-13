---
title: Установка и регистрация обработчиков протоколов (устаревшие функции среды Windows)
description: Установка обработчиков протоколов включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files и их регистрацию.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340265"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a><span data-ttu-id="b3f6b-103">Установка и регистрация обработчиков протоколов (устаревшие функции среды Windows)</span><span class="sxs-lookup"><span data-stu-id="b3f6b-103">Installing and Registering Protocol Handlers (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="b3f6b-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b3f6b-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="b3f6b-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="b3f6b-106">Установка **обработчиков протоколов** включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files и их регистрацию.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-106">Installing **protocol handlers** involves copying the DLL(s) to an appropriate location in the Program Files directory and registering them.</span></span>

<span data-ttu-id="b3f6b-107">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="b3f6b-108">Рекомендации по установке</span><span class="sxs-lookup"><span data-stu-id="b3f6b-108">Installation Guidelines</span></span>](#installation-guidelines)
-   [<span data-ttu-id="b3f6b-109">Регистрация обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="b3f6b-109">To Register Protocol Handlers</span></span>](#to-register-protocol-handlers)
-   [<span data-ttu-id="b3f6b-110">Регистрация расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="b3f6b-110">To Register Shell Extensions</span></span>](#to-register-shell-extensions)

## <a name="installation-guidelines"></a><span data-ttu-id="b3f6b-111">Рекомендации по установке</span><span class="sxs-lookup"><span data-stu-id="b3f6b-111">Installation Guidelines</span></span>

<span data-ttu-id="b3f6b-112">Обработчики протоколов должны реализовать самостоятельную регистрацию для установки и следовать приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-112">Protocol handlers should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="b3f6b-113">Установщик должен использовать установщик EXE или MSI.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-113">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="b3f6b-114">Необходимо указать заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-114">Release notes must be provided.</span></span>
-   <span data-ttu-id="b3f6b-115">Для каждой установленной надстройки необходимо создать запись « **Установка и удаление программ** ».</span><span class="sxs-lookup"><span data-stu-id="b3f6b-115">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="b3f6b-116">Установщик должен задействовать все параметры реестра для конкретного типа файлов или хранить данные, распознаваемые текущей надстройкой.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-116">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="b3f6b-117">Если предыдущая надстройка перезаписывается, установщик должен уведомить пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-117">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="b3f6b-118">Если более новая надстройка перезаписала предыдущую надстройку, то должна быть возможность восстановить функциональность предыдущей надстройки и сделать ее надстройкой по умолчанию для этого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-118">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>

## <a name="to-register-protocol-handlers"></a><span data-ttu-id="b3f6b-119">Регистрация обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="b3f6b-119">To Register Protocol Handlers</span></span>

<span data-ttu-id="b3f6b-120">Для регистрации компонента обработчика протокола необходимо внести в реестр записи четырнадцать, где:</span><span class="sxs-lookup"><span data-stu-id="b3f6b-120">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="b3f6b-121">*Версия \_ Параметр \_* "DIB ProgID" — это независимый от версии идентификатор ProgID реализации обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="b3f6b-121">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="b3f6b-122">*Версия \_ DEP \_ ProgID* — это зависимый от версии идентификатор ProgID реализации обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-122">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="b3f6b-123">*CLSID \_ 1* — это CLSID реализации обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="b3f6b-123">*CLSID\_1* is the CLSID of the protocol handler implementation</span></span>

1.  <span data-ttu-id="b3f6b-124">Зарегистрируйте независимый от версии идентификатор ProgID со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="b3f6b-124">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="b3f6b-125">Зарегистрируйте версию ProgID, зависимую от версии, со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="b3f6b-125">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="b3f6b-126">Зарегистрируйте CLSID обработчика протокола со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="b3f6b-126">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  <span data-ttu-id="b3f6b-127">Регистрация обработчика протокола с помощью службы поиска Windows Desktop:</span><span class="sxs-lookup"><span data-stu-id="b3f6b-127">Register the protocol handler with Windows Desktop Search:</span></span>

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a><span data-ttu-id="b3f6b-128">Регистрация расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="b3f6b-128">To Register Shell Extensions</span></span>

<span data-ttu-id="b3f6b-129">Чтобы зарегистрировать расширение оболочки обработчика протокола, необходимо создать две записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="b3f6b-129">You need to make two entries in the registry to register the protocol handler's Shell extension.</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




