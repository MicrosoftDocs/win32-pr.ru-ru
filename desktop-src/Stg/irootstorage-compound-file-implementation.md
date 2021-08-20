---
title: Ирутстораже — реализация составного файла
description: Реализация Ирутстораже для составных файлов COM позволяет сохранять файлы в ситуациях нехватки памяти или нехватке места на диске. Сведения о работе этого интерфейса см. в разделе Ирутстораже.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- Ирутстораже Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20128e749443d19c6418703bf64d93eb763ae25103d677719bb4cb4cd21349a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961202"
---
# <a name="irootstorage---compound-file-implementation"></a>Ирутстораже — реализация составного файла

Реализация [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) для составных файлов com позволяет сохранять файлы в ситуациях нехватки памяти или нехватке места на диске. Сведения о работе этого интерфейса см. в разделе **ирутстораже**.

## <a name="when-to-use"></a>Назначение

Используйте предоставляемую системой реализацию [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) только для поддержки сохранения файлов в условиях нехватки памяти.

## <a name="remarks"></a>Remarks

Для выполнения обычной операции сохранения в другом файле можно вызвать реализацию [**ирутстораже:: свитчтофиле**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) в com. Однако приложения, которые это делают, могут быть несовместимы с будущими поколениями хранилища COM. Чтобы избежать этой ситуации, приложения, выполняющие операцию "Сохранить как", должны вручную создать второй составной файл и вызвать метод [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). Метод **ирутстораже:: свитчтофиле** следует использовать только в экстренных ситуациях (нехватка памяти или дискового пространства).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**Ирутстораже:: Свитчтофиле**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




