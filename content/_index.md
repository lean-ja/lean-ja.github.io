+++
title = "lean ja"
sort_by = "weight"
+++

## __Lean について__

[Lean](https://leanprover.github.io/) は容易に正しく保守性の高いコードを書くことができるよう設計された，純粋関数型言語です．依存型という表現力の高い型システムを備えており，アルゴリズムなどが本当に意図したものを返すことを証明することができます．

Lean は証明支援系でもあり，数学の証明を検証する能力を備えています．Lean で証明を書いている限り，コンパイルが通れば証明は正しいと自信を持つことができます．

そして Lean はパワフルです．いま示すべきことと得られていることを逐一表示できるのはもちろん，証明の一部を自動化したり，強すぎる仮定を自動的に検出したりすることもできます．

```lean
import Mathlib.Tactic

/-- フィボナッチ数列の線形時間の実装 -/
def fib (n : Nat) : Nat :=
  (loop n).1
where
  -- ヘルパー関数を定義する
  loop : Nat → Nat × Nat
    | 0   => (0, 1)
    | n + 1 =>
      let p := loop n
      (p.2, p.1 + p.2)

-- 最初の数個の値に対してテストする
#guard [0, 1, 2, 3, 4, 5].map fib = [0, 1, 1, 2, 3, 5]

/-- `fib` が満たす漸化式 -/
theorem fib_add (n : Nat) : fib n + fib (n + 1) = fib (n + 2) := by rfl
```

現在，Lean で数学理論を実装していこうという努力が積極的に行われています．[mathlib4](https://github.com/leanprover-community/mathlib4) というライブラリがあり，大学の学部程度の数学のかなりの部分を Lean で行うことが可能になっています．

[Lean 4 Web](https://live.lean-lang.org/) から Lean を試すことができます．あなたも Lean で新しい数学を体験してみませんか？
