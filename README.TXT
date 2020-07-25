Rt Calculator Worksheet

1 概要
本ワークシートは、新型コロナウィルス等の実効再生産数を計算するために作成されたものです。Excel上で動作しますが、マクロやその他特殊機能を一切使わずセル間の関係式のみで計算しているため、他の表計算ソフトでも動作する可能性が高いと思われます。

2 使い方

「Rt計算」シートのA列に日付、B列に陽性判明者数を入力します。B列の4行め以降については、最新の数字より上のセルに0を含めて何らかの数字が入力され、かつそれより後は空欄である必要があります。報告率を考慮するために、最新の数字の位置を特定する目的でこのような仕様になっています。

入力が終わると同時に「グラフ」シートに結果が表示されます。「Rt計算」シートのFからK列については、表示させたい範囲に応じてコピー・ペースト、あるいは削除して調整してください。またグラフについても、表示される日付の範囲は自動で変更されないため、データに応じて適当に設定してください。（いずれ自動で変更されるように回収します。）

「data」シートには、
・感染日から報告日（確定日）までの日数の分布（PDF）を0日から順に並べたもの
・二次感染日から報告日（確定日）までの日数の分布（PDF）を0日から順に並べたもの
・感染日から報告日（確定日）までの日数の累積分布（CDF）を0日から50日まで順に並べたもの
・二次感染日から報告日（確定日）までの日数の累積分布（CDF）を-20日から50日まで順に並べたもの
を入力します。すでに入っている値でも分析できますが、違う分布で試したい場合はこれらを変更します。

3 計算ロジック

一般的な「報告数の数列を逆畳み込みをする」という手法とは異なり、「報告日と各事象までの日数分布に従った数を報告日から引く」ことにより、感染日や2次感染日を推定しています。
https://twitter.com/p_gotcha/status/1278646135309996039
に解説していますがこのワークシートではまた少し異なり、乱数を使わずに計算しています。計算の過程については「計算過程」シートをご覧ください。

4 著作権等

著作権等に関してはApache License 2.0を適用します。何かで使用された場合は、事後で構いませんので連絡をいただけたら幸いです。

Copyright 2020 Pitchblende(@p_gotcha)

Licensed under the Apache License, Version 2.0 (the “License”);
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an “AS IS” BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.