---
description: Это событие элемента управления выполняет указанный файл. Если файл не существует или происходит сбой события, установщик Windows регистрирует ошибку в подробном журнале без отображения диалогового окна, содержащего сообщение об ошибке.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: Мсилаунчапп таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650640"
---
# <a name="msilaunchapp-controlevent"></a><span data-ttu-id="1afd5-104">Мсилаунчапп таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="1afd5-104">MsiLaunchApp ControlEvent</span></span>

<span data-ttu-id="1afd5-105">Это событие элемента управления выполняет указанный файл.</span><span class="sxs-lookup"><span data-stu-id="1afd5-105">This control event runs a specified file.</span></span> <span data-ttu-id="1afd5-106">Если файл не существует или происходит сбой события, установщик Windows регистрирует ошибку в подробном журнале без отображения диалогового окна, содержащего сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1afd5-106">If the file does not exist, or if the event fails, Windows Installer logs the error in the verbose log without displaying a dialog box containing an error message.</span></span>

<span data-ttu-id="1afd5-107">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1afd5-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="1afd5-108">Этот таблице ControlEvent событие доступен начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="1afd5-108">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

## <a name="published-by"></a><span data-ttu-id="1afd5-109">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="1afd5-109">Published By</span></span>

<span data-ttu-id="1afd5-110">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="1afd5-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1afd5-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="1afd5-111">Argument</span></span>

<span data-ttu-id="1afd5-112">Поля значения аргумента разделяются пробелами.</span><span class="sxs-lookup"><span data-stu-id="1afd5-112">The fields of the argument value are delimited by spaces.</span></span> <span data-ttu-id="1afd5-113">Первое поле содержит строковое значение, указывающее файл, который должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="1afd5-113">The first field contains a string value that specifies the file that is to be run.</span></span> <span data-ttu-id="1afd5-114">Используйте строковое значение \[ \# *филекэй* \] для идентификации файла и замены *филекэй* на идентификатор файла, отображаемый в столбце File таблицы [File](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1afd5-114">Use a string value of \[\#*filekey*\] to identify the file and replace *filekey* with the file's identifier appearing in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="1afd5-115">Все оставшиеся поля аргумента могут содержать параметры, используемые запускаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="1afd5-115">Any remaining fields of the argument can contain parameters being used by the file being run.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1afd5-116">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="1afd5-116">Action on Subscribers</span></span>

<span data-ttu-id="1afd5-117">Эта таблице ControlEvent событие не выполняет никаких действий на подписчиках.</span><span class="sxs-lookup"><span data-stu-id="1afd5-117">This ControlEvent performs no actions on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1afd5-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="1afd5-118">Typical Use</span></span>

<span data-ttu-id="1afd5-119">, Чтобы разрешить пользователю выбрать запуск файла в конце установки.</span><span class="sxs-lookup"><span data-stu-id="1afd5-119">To enable a user to choose to run a file at the end of an installation.</span></span> <span data-ttu-id="1afd5-120">Это событие может быть задано для свойства, установленного элементом управления [CheckBox](checkbox-control.md) , который отображается в последнем диалоговом окне установки.</span><span class="sxs-lookup"><span data-stu-id="1afd5-120">This event can be conditioned on a property set by a [CheckBox](checkbox-control.md) control displayed on the final dialog box of the installation.</span></span> <span data-ttu-id="1afd5-121">Элемент управления CheckBox не должен отображаться во время удаления пакета.</span><span class="sxs-lookup"><span data-stu-id="1afd5-121">The CheckBox control should not be displayed during the removal of the package.</span></span>

 

 



