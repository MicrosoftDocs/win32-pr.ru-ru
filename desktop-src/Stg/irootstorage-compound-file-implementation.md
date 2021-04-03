---
title: Ирутстораже — реализация составного файла
description: Реализация Ирутстораже для составных файлов COM позволяет сохранять файлы в ситуациях нехватки памяти или нехватке места на диске. Сведения о работе этого интерфейса см. в разделе Ирутстораже.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- Ирутстораже Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780105"
---
# <a name="irootstorage---compound-file-implementation"></a>Ирутстораже — реализация составного файла

Реализация [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) для составных файлов com позволяет сохранять файлы в ситуациях нехватки памяти или нехватке места на диске. Сведения о работе этого интерфейса см. в разделе **ирутстораже**.

## <a name="when-to-use"></a>Назначение

Используйте предоставляемую системой реализацию [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) только для поддержки сохранения файлов в условиях нехватки памяти.

## <a name="remarks"></a>Комментарии

Для выполнения обычной операции сохранения в другом файле можно вызвать реализацию [**ирутстораже:: свитчтофиле**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) в com. Однако приложения, которые это делают, могут быть несовместимы с будущими поколениями хранилища COM. Чтобы избежать этой ситуации, приложения, выполняющие операцию "Сохранить как", должны вручную создать второй составной файл и вызвать метод [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). Метод **ирутстораже:: свитчтофиле** следует использовать только в экстренных ситуациях (нехватка памяти или дискового пространства).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**Ирутстораже:: Свитчтофиле**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




