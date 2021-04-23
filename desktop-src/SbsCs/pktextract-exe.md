---
description: Pktextract.exe — это средство, которое извлекает атрибут publicKeyToken из файла сертификата.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156147"
---
# <a name="pktextractexe"></a><span data-ttu-id="03f25-103">Pktextract.exe</span><span class="sxs-lookup"><span data-stu-id="03f25-103">Pktextract.exe</span></span>

<span data-ttu-id="03f25-104">Pktextract.exe — это средство, которое извлекает атрибут **PublicKeyToken** из файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="03f25-104">Pktextract.exe is a tool that extracts the **publicKeyToken** attribute from a certificate file.</span></span> <span data-ttu-id="03f25-105">Выходные данные — это **PublicKeyToken**, который представляет собой уникальный 16-символьный (8-байтовый) идентификатор открытого ключа, присутствующего в сертификате, в формате, который можно легко вставлять в инструкцию Identity.</span><span class="sxs-lookup"><span data-stu-id="03f25-105">The output is the **publicKeyToken**, which is a unique 16-character (8-byte) identifier of the public key present in the certificate, in a format that can easily be pasted into an assembly identity statement.</span></span> <span data-ttu-id="03f25-106">Файл сертификата должен находиться в том же каталоге, что и Pktextract.exe для использования программы.</span><span class="sxs-lookup"><span data-stu-id="03f25-106">The certificate file must be present in the same directory as Pktextract.exe to use the utility.</span></span> <span data-ttu-id="03f25-107">Pktextract.exe предоставляется в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="03f25-107">Pktextract.exe is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="03f25-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03f25-108">Syntax</span></span>

<span data-ttu-id="03f25-109">**pktextract.exe** *<имя_файла. cer>* **\[ -quiet \] \[ -Logo \]**</span><span class="sxs-lookup"><span data-stu-id="03f25-109">**pktextract.exe** *<filename.cer>* **\[-quiet\] \[-nologo\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="03f25-110">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="03f25-110">Command Line Options</span></span>

<span data-ttu-id="03f25-111">В Pktextract.exe используются следующие параметры командной строки без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="03f25-111">Pktextract.exe uses the following case-insensitive command line options.</span></span>



| <span data-ttu-id="03f25-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="03f25-112">Option</span></span>  | <span data-ttu-id="03f25-113">Описание</span><span class="sxs-lookup"><span data-stu-id="03f25-113">Description</span></span>                                                          |
|---------|----------------------------------------------------------------------|
| <span data-ttu-id="03f25-114">-quiet</span><span class="sxs-lookup"><span data-stu-id="03f25-114">-quiet</span></span>  | <span data-ttu-id="03f25-115">Подавляет полный вывод сведений о сертификате.</span><span class="sxs-lookup"><span data-stu-id="03f25-115">Suppresses full display of certificate information.</span></span> <span data-ttu-id="03f25-116">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="03f25-116">Optional.</span></span>        |
| <span data-ttu-id="03f25-117">-nologo</span><span class="sxs-lookup"><span data-stu-id="03f25-117">-nologo</span></span> | <span data-ttu-id="03f25-118">Выполняется без отображения стандартных данных об авторских правах Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="03f25-118">Runs without displaying standard Microsoft copyright data.</span></span> <span data-ttu-id="03f25-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="03f25-119">Optional.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="03f25-120">См. также</span><span class="sxs-lookup"><span data-stu-id="03f25-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03f25-121">Средства разработки параллельных сборок</span><span class="sxs-lookup"><span data-stu-id="03f25-121">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



