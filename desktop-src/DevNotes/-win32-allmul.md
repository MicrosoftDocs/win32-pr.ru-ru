---
title: _allmul подпрограммы
description: Умножает два целых числа ЛОНГЛОНГ или УЛОНГЛОНГ.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "104069481"
---
# <a name="_allmul-routine"></a>\_подпрограммы аллмул

Умножает два целых числа **лонглонг** или **улонглонг** .
Например, чтобы умножить два значения Int64, компилятор может создать вызов подпрограммы **\_ аллмул** .

## <a name="remarks"></a>Комментарии

Подпрограммы **\_ аллмул** — это вспомогательная подпрограммы для компилятора C.
Будет ли компилятор использовать **\_ аллмул** , полностью зависит от набора оптимизации.

Эта подпрограммы используется только на платформах x86.
