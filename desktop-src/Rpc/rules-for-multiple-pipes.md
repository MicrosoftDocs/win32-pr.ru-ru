---
title: Правила для нескольких каналов
description: Правила для нескольких каналов в одном вызове в удаленном вызове процедур (RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd2de7a44f63d5c943f1d6526ee328bbae3e63c99bac118ec843ad266d1f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925981"
---
# <a name="rules-for-multiple-pipes"></a>Правила для нескольких каналов

В \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] \[  \] любом сочетании в одном вызове можно сочетать параметры вертикального канала, out и in, но необходимо обработать каналы в определенном порядке, как показано в следующем примере псевдокода:

> [!Note]  
> эта функция больше не поддерживается в Windows Vista и более поздних платформах.

 

-   Получите данные из каждого входного канала, начиная с первого (крайнего левого) \[ **в** \] параметре, и продолжая по порядку выполнять сток каждого канала перед началом обработки следующего.
-   После полной обработки каждого входного канала отправьте данные для выходных каналов, снова начиная с первого \[ **выходного** \] параметра и продолжая по порядку, заполняя каждый канал перед началом обработки следующего.

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 